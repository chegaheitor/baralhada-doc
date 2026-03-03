# Mensagens

## 💬 O que são as Mensagens do Bot

Cada ação (abrir pacote, ganhar carta, erro de saldo) tem uma mensagem correspondente. Você pode usar "Variáveis" (placeholders) para que o bot insira nomes, valores e itens automaticamente. Dê uma voz única ao seu bot.

### 🛠️ Editando uma Mensagem

{% stepper %}
{% step %}
## Vá em Painel → Mensagens

Navegue pelas categorias (Economia, Itens, Social, Erros).
{% endstep %}

{% step %}
## Escolha o Template

Clique na mensagem que deseja traduzir ou personalizar.
{% endstep %}

{% step %}
## Use as Variáveis

Edite o texto mantendo as palavras entre chaves `{}` para que o bot as preencha.
{% endstep %}

{% step %}
### Adicione Emojis

Dê personalidade ao seu texto, adicione emojis e emotes próprios do seu canal da twitch!
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Não remova as chaves: Se você apagar o \`{item}\`, o bot não dirá qual carta o viewer ganhou!&#x20;
{% endhint %}

## 🎭 Tom de Voz (Branding)

A mensagem é como o seu bot faz a conexão entre Você <-> Baralhada <-> Viewers, é importante saber como dizer &#x20;

* **Impacto**: O bot é uma extensão da sua live. Se você é um streamer zoeiro, faça mensagens divertidas. Se é sério, mantenha a clareza técnica.

{% hint style="warning" %}
**Cuidado:** Fuja de mensagens gigantescas! A Twitch pode "cortar" mensagens muito longas ou o bot pode ser silenciado por mandar blocos de texto muito grandes.
{% endhint %}

## 📋 Lista de Variáveis por Categoria

Abaixo estão todas as variáveis disponíveis, organizadas por onde elas aparecem.

<details>

<summary>🌐 Gerais e Sistema</summary>

<table><thead><tr><th width="176">Variável</th><th>Descrição</th></tr></thead><tbody><tr><td><code>{user}</code> ou <code>{username}</code></td><td>Nome do espectador que acionou o comando.</td></tr><tr><td><code>{target}</code></td><td>Nome do usuário alvo (em comandos de admin ou trocas).</td></tr><tr><td><code>{time}</code></td><td>Tempo restante ou duração (em segundos ou formatado).</td></tr><tr><td><code>{latency}</code></td><td>Latência do bot (usado no !ping).</td></tr><tr><td><code>{usage}</code></td><td>Exemplo de uso correto de um comando.</td></tr><tr><td><code>{requiredRole}</code></td><td>Cargo necessário para usar um comando.</td></tr><tr><td><code>{level}</code></td><td>Nível atual do usuário.</td></tr></tbody></table>

</details>

<details>

<summary>📦 Spawns e Resgates</summary>

<table><thead><tr><th width="181">Variável</th><th>Descrição</th></tr></thead><tbody><tr><td><code>{packName}</code></td><td>Nome do pacote que apareceu.</td></tr><tr><td><code>{packId}</code></td><td>ID (slug) do pacote.</td></tr><tr><td><code>{command}</code></td><td>Comando para resgatar (ex: !resgatar).</td></tr><tr><td><code>{customMessage}</code></td><td>Mensagem personalizada configurada no pacote.</td></tr><tr><td><code>{winners}</code></td><td>Lista de ganhadores de um sorteio.</td></tr></tbody></table>

</details>

<details>

<summary>🃏 Cartas e Pacotes</summary>

<table><thead><tr><th width="145">Variável</th><th>Descrição</th></tr></thead><tbody><tr><td><code>{item}</code></td><td>Nome da carta ou pacote envolvido na ação.</td></tr><tr><td><code>{cards}</code></td><td>Lista de cartas ganhas ao abrir um pacote.</td></tr><tr><td><code>{extra}</code></td><td>Bônus ou informações adicionais na abertura.</td></tr><tr><td><code>{rarity}</code></td><td>Raridade da carta.</td></tr><tr><td><code>{number}</code></td><td>Número da carta na coleção.</td></tr><tr><td><code>{types}</code></td><td>Tipos da carta (ex: Fogo / Dragão).</td></tr><tr><td><code>{stats}</code></td><td>Atributos da carta (HP, Ataque, etc).</td></tr><tr><td><code>{desc}</code></td><td>Descrição/Lore da carta.</td></tr></tbody></table>

</details>

<details>

<summary>💰 Economia e Loja</summary>

<table><thead><tr><th width="134">Variável</th><th>Descrição</th></tr></thead><tbody><tr><td><code>{points}</code></td><td>Saldo atual de pontos do usuário.</td></tr><tr><td><code>{price}</code></td><td>Preço de compra ou venda do item.</td></tr><tr><td><code>{amount}</code></td><td>Quantidade de pontos ganhos ou alterados.</td></tr><tr><td><code>{total}</code></td><td>Novo saldo total após uma alteração.</td></tr><tr><td><code>{link}</code></td><td>Link da página da loja.</td></tr></tbody></table>

</details>

<details>

<summary>🤝 Trocas e Social</summary>

| Variável              | Descrição                                |
| --------------------- | ---------------------------------------- |
| `{src}`               | Usuário que iniciou a troca ou presente. |
| `{itemA}` / `{itemB}` | Itens envolvidos na proposta de troca.   |
| `{userA}` / `{userB}` | Participantes da troca concluída.        |

</details>

<details>

<summary>🎯 Missões e Conquistas</summary>

| Variável            | Descrição                                  |
| ------------------- | ------------------------------------------ |
| `{title}`           | Título da missão.                          |
| `{progress}`        | Progresso atual (ex: 5).                   |
| `{goal}`            | Meta da missão (ex: 10).                   |
| `{reward}`          | Recompensa da missão (pontos, packs, etc). |
| `{achievementName}` | Nome da conquista desbloqueada.            |
| `{achievementDesc}` | Descrição da conquista.                    |

</details>

## ✨ Emojis e Emotes

Você pode personalizar suas mensagens utilizando tanto emojis padrão quanto os emotes do seu próprio canal da Twitch. Para que o bot consiga enviar seus emotes personalizados, certifique-se de que ele possui os cargos necessários (como moderador ou inscrito).

## ⚡ Atualização em Tempo Real

As alterações nas mensagens são aplicadas em tempo real. Assim que você salvar as modificações no painel, o bot passará a usar os novos textos imediatamente, sem a necessidade de reiniciar o programa ou o bot.
