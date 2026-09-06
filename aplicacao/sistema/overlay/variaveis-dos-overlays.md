# 📖 Variáveis dos Overlays

## 💡 Como funcionam as variáveis

Quando um evento acontece na transmissão (um pacote surge, um espectador abre cartas, um duelo é finalizado, etc.), o Baralhada injeta automaticamente todos os dados relevantes.

Você pode utilizar as variáveis de **duas formas**:

#### Forma 1: No HTML (Interpolação Direta)

Basta colocar o nome da variável entre chaves duplas `{{ ... }}`. O sistema substituirá automaticamente antes de exibir no OBS:

```html
<div class="meu-alerta">
  <img src="{{data.userAvatar}}" alt="Avatar" class="avatar-redondo" />
  <h2>@{{data.userName}} acabou de abrir um {{data.packName}}!</h2>
  <p>Saldo do viewer: {{data.userCoins}} {{data.currencyName}}</p>
</div>
```

{% hint style="info" %}
Você pode escrever tanto `{{data.userName}}` quanto `{{userName}}`, ambos funcionam perfeitamente
{% endhint %}

***

#### Forma 2: No JavaScript (`window.overlayData`)

Se você precisa de lógica condicional (ex: tocar som especial se for carta lendária, fazer cálculos de vida ou rodar animações), acesse o objeto global `window.overlayData`:

```html
<script>
  const evento = window.overlayData;
  console.log("Usuário:", evento.userName);
  console.log("Moedas:", evento.userCoins);

  // Exemplo: tocar áudio se a carta for Lendária
  if (evento.cardRarity && evento.cardRarity.toLowerCase().includes('lend')) {
    const audioEpico = new Audio('https://seusite.com/som_lendario.mp3');
    audioEpico.volume = 0.9;
    audioEpico.play();
  }
</script>
```

***

## 🗂️ Catálogo geral de variáveis por categoria

Todas as variáveis abaixo estão disponíveis e funcionam em **todos os overlays** do sistema.

### 👤 Viewer & Espectador

Variáveis relacionadas ao espectador que participou ou acionou o evento.

| Variável                    | Tipo     | O Que É e O Que Faz                                            | Exemplo de Valor                   |
| --------------------------- | -------- | -------------------------------------------------------------- | ---------------------------------- |
| `{{data.userName}}`         | `string` | Nome de usuário da Twitch do espectador em minúsculas          | `viewer_name`                      |
| `{{data.userDisplayName}}`  | `string` | Nome de exibição formatado com maiúsculas/minúsculas da Twitch | `Viewer_name`                      |
| `{{data.userAvatar}}`       | `url`    | Link da imagem da foto de perfil da Twitch do espectador       | `https://static-cdn.jtvnw.net/...` |
| `{{data.userCoins}}`        | `number` | Quantidade atual de moedas/pontos que o espectador possui      | `1450`                             |
| `{{data.userPacksCount}}`   | `number` | Total de pacotes fechados que o espectador tem no inventário   | `5`                                |
| `{{data.userCardsCount}}`   | `number` | Quantidade total de cartas que o espectador já colecionou      | `52`                               |
| `{{data.userCardsPercent}}` | `number` | Porcentagem estimada de conclusão da coleção de cartas         | `74`                               |

***

### 🎴 Cartas & Coleção

Variáveis relacionadas às cartas exibidas, inspecionadas ou reveladas.

| Variável                   | Tipo      | O Que É e O Que Faz                                                         | Exemplo de Valor                   |
| -------------------------- | --------- | --------------------------------------------------------------------------- | ---------------------------------- |
| `{{data.cardName}}`        | `string`  | Nome da carta principal em destaque                                         | `Dragão Cósmico Ancestral`         |
| `{{data.cardImage}}`       | `url`     | Link da arte/imagem oficial da carta                                        | `/uploads/dragao_cosmico.png`      |
| `{{data.cardRarity}}`      | `string`  | Nome da raridade da carta (`Comum`, `Incomum`, `Rara`, `Épica`, `Lendária`) | `Lendária`                         |
| `{{data.cardRarityColor}}` | `string`  | Código hexadecimal da cor oficial da raridade (ideal para bordas e sombras) | `#f59e0b`                          |
| `{{data.cardPower}}`       | `number`  | Poder de ataque da carta (para batalhas/duelos)                             | `95`                               |
| `{{data.cardDefense}}`     | `number`  | Defesa / resistência da carta                                               | `80`                               |
| `{{data.cardDescription}}` | `string`  | Texto descritivo de efeito, história ou lore da carta                       | `Guardião lendário dos céus.`      |
| `{{data.cardNumber}}`      | `number`  | Número oficial da carta no álbum                                            | `14`                               |
| `{{data.cardIsNew}}`       | `boolean` | Retorna `true` se é a primeira vez que o espectador ganha essa carta        | `true`                             |
| `{{data.cardsCount}}`      | `number`  | Quantidade total de cartas envolvidas no evento                             | `3`                                |
| `{{data.cards}}`           | `array`   | _(Apenas JS)_ Lista com todas as cartas abertas no pacote                   | `[{ name, image, rarity, isNew }]` |

***

### 📦 Pacotes & Drops

Variáveis relacionadas aos pacotes de cartas, drops no chat e resgates.

| Variável                    | Tipo     | O Que É e O Que Faz                               | Exemplo de Valor         |
| --------------------------- | -------- | ------------------------------------------------- | ------------------------ |
| `{{data.packName}}`         | `string` | Nome do pacote em exibição ou dropado na live     | `Pacote Lendário Alfa`   |
| `{{data.packCover}}`        | `url`    | Imagem da arte de capa do pacote                  | `/uploads/pack_alfa.png` |
| `{{data.packCost}}`         | `number` | Preço de compra do pacote na loja em moedas       | `250`                    |
| `{{data.packCardsPerPack}}` | `number` | Quantidade de cartas geradas ao abrir este pacote | `3`                      |
| `{{data.packCategory}}`     | `string` | Categoria ou edição do pacote                     | `Edição de Lançamento`   |
| `{{data.claimCommand}}`     | `string` | Comando do chat configurado para resgatar o drop  | `!resgatar`              |

***

### 📺 Canal & Transmissão

Variáveis gerais sobre a live, o canal e o sistema do Baralhada.

| Variável                   | Tipo     | O Que É e O Que Faz                                                | Exemplo de Valor               |
| -------------------------- | -------- | ------------------------------------------------------------------ | ------------------------------ |
| `{{data.channelName}}`     | `string` | Nome do canal da Twitch configurado                                | `baralhada_live`               |
| `{{data.botName}}`         | `string` | Nome do bot conectado ao chat                                      | `BaralhadaBot`                 |
| `{{data.currencyName}}`    | `string` | Nome da moeda do canal configurada no app (ex: `Pontos`, `Moedas`) | `Baralhacoins`                 |
| `{{data.streamerName}}`    | `string` | Nome do streamer dono do canal                                     | `Heitor`                       |
| `{{data.date}}`            | `string` | Data atual formatada (DD/MM/AAAA)                                  | `06/09/2026`                   |
| `{{data.time}}`            | `string` | Horário atual formatado (HH:MM:SS)                                 | `11:30:15`                     |
| `{{data.timestamp}}`       | `number` | Timestamp numérico em milissegundos                                | `1788708615000`                |
| `{{data.overlayType}}`     | `string` | Identificador do tipo de overlay ativo                             | `spawn`, `duel`, `pack_opened` |
| `{{data.overlayDuration}}` | `number` | Tempo de exibição configurado em segundos                          | `10`                           |

***

### ⚔️ Eventos Específicos

Variáveis presentes em eventos de interação entre múltiplos espectadores.

#### **Duelo de Cartas (`duel`)**

| Variável                | Tipo     | O Que É e O Que Faz                   | Exemplo             |
| ----------------------- | -------- | ------------------------------------- | ------------------- |
| `{{data.winnerName}}`   | `string` | Nome do espectador que venceu o duelo | `campeao_twitch`    |
| `{{data.winnerAvatar}}` | `url`    | Avatar do vencedor do duelo           | `https://...`       |
| `{{data.winnerHP}}`     | `number` | Pontos de vida restantes do vencedor  | `45`                |
| `{{data.loserName}}`    | `string` | Nome do espectador derrotado no duelo | `desafiante_twitch` |
| `{{data.loserAvatar}}`  | `url`    | Avatar do derrotado no duelo          | `https://...`       |
| `{{data.duelBet}}`      | `number` | Valor de moedas apostadas no duelo    | `500`               |

#### **Troca de Cartas (`trade`)**

| Variável              | Tipo     | O Que É e O Que Faz                    | Exemplo          |
| --------------------- | -------- | -------------------------------------- | ---------------- |
| `{{data.tradeUserA}}` | `string` | Nome do primeiro jogador na troca      | `colecionador_1` |
| `{{data.tradeUserB}}` | `string` | Nome do segundo jogador na troca       | `colecionador_2` |
| `{{data.tradeItemA}}` | `string` | Nome da carta oferecida pelo jogador 1 | `Mago Negro`     |
| `{{data.tradeItemB}}` | `string` | Nome da carta oferecida pelo jogador 2 | `Dragão Branco`  |

#### **Presente no Chat (`gift`)**

| Variável                  | Tipo     | O Que É e O Que Faz             | Exemplo           |
| ------------------------- | -------- | ------------------------------- | ----------------- |
| `{{data.senderName}}`     | `string` | Nome de quem enviou o presente  | `generoso_viewer` |
| `{{data.senderAvatar}}`   | `url`    | Foto de perfil de quem enviou   | `https://...`     |
| `{{data.receiverName}}`   | `string` | Nome de quem recebeu o presente | `amigo_viewer`    |
| `{{data.receiverAvatar}}` | `url`    | Foto de perfil de quem recebeu  | `https://...`     |

#### **Cofre da Sorte (`cofre_winner`)**

| Variável                | Tipo     | O Que É e O Que Faz                 | Exemplo          |
| ----------------------- | -------- | ----------------------------------- | ---------------- |
| `{{data.winnerName}}`   | `string` | Nome de quem abriu o cofre da sorte | `sortudo_viewer` |
| `{{data.winnerAvatar}}` | `url`    | Avatar do ganhador do cofre         | `https://...`    |
| `{{data.packName}}`     | `string` | Nome do pacote ganho no cofre       | `Pacote Mítico`  |

***

## 🎨 Exemplos Práticos de Código

#### Exemplo 1: Card de Viewer com Foto Redonda e Brilho Neon

```html
<style>
  .viewer-card {
    display: flex;
    align-items: center;
    gap: 16px;
    background: rgba(16, 24, 40, 0.95);
    border: 2px solid #2563ff;
    padding: 14px 20px;
    border-radius: 20px;
    box-shadow: 4px 4px 0px #2563ff;
    color: white;
    font-family: sans-serif;
  }
  .avatar {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    border: 3px solid #00e5ff;
    object-fit: cover;
  }
</style>

<div class="viewer-card">
  <img src="{{data.userAvatar}}" alt="{{data.userName}}" class="avatar" />
  <div>
    <h3 style="margin: 0;">@{{data.userDisplayName}}</h3>
    <span style="color: #c8ff3d; font-size: 13px;">💰 Saldo: {{data.userCoins}} {{data.currencyName}}</span>
  </div>
</div>
```

***

#### Exemplo 2: Borda e Brilho Dinâmicos de Acordo com a Raridade da Carta

Use `{{data.cardRarityColor}}` para colorir a borda e a sombra automaticamente:

```html
<style>
  .carta-container {
    background: #101828;
    border-radius: 24px;
    padding: 16px;
    border: 3px solid {{data.cardRarityColor}};
    box-shadow: 0 0 25px {{data.cardRarityColor}};
    text-align: center;
    color: white;
    width: 260px;
  }
  .raridade-tag {
    color: {{data.cardRarityColor}};
    font-weight: bold;
    text-transform: uppercase;
    font-size: 12px;
  }
</style>

<div class="carta-container">
  <img src="{{data.cardImage}}" style="width: 100%; border-radius: 14px;" />
  <h2 style="margin: 10px 0 4px 0;">{{data.cardName}}</h2>
  <span class="raridade-tag">✦ {{data.cardRarity}} ✦</span>
</div>
```

***

#### Exemplo 3: Listar Todas as Cartas Abertas via JavaScript

```html
<div id="lista-cartas" style="display: flex; gap: 15px; justify-content: center;"></div>

<script>
  const dados = window.overlayData;
  const container = document.getElementById('lista-cartas');

  if (dados.cards && Array.isArray(dados.cards)) {
    dados.cards.forEach(carta => {
      const cardEl = document.createElement('div');
      cardEl.style.cssText = 'background: #101828; border: 2px solid #2563ff; border-radius: 16px; padding: 10px; text-align: center; color: white; width: 180px;';
      cardEl.innerHTML = `
        <img src="${carta.image}" style="width: 100%; border-radius: 10px;" />
        <h4 style="margin: 8px 0 2px 0; font-size: 14px;">${carta.name}</h4>
        <small style="color: #c8ff3d;">${carta.rarity}</small>
        ${carta.isNew ? '<span style="display:block; background:#c8ff3d; color:#101828; font-weight:bold; font-size:10px; border-radius:4px; margin-top:4px;">NOVA!</span>' : ''}
      `;
      container.appendChild(cardEl);
    });
  }
</script>
```

***

## ❓ Perguntas Frequentes

<details>

<summary><strong>Posso usar <code>{{userName}}</code> ou precisa ser <code>{{data.userName}}</code>?</strong></summary>

Ambos funcionam! O motor de template do Baralhada aceita tanto `{{data.userName}}` quanto `{{userName}}`.

</details>

<details>

<summary><strong>Como testar minhas alterações?</strong></summary>

Dentro do modal de personalização, clique no botão **"Testar no OBS"** no canto superior direito para disparar o evento ao vivo na fonte do OBS!

</details>

<details>

<summary><strong>E se meu código quebrar?</strong></summary>

Basta clicar no botão vermelho **"Restaurar Padrão"** na barra superior do editor para voltar instantaneamente ao layout original de fábrica.

</details>
