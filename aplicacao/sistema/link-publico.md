# 🌐 Link Público

O **Link Público** é uma funcionalidade que permite que os espectadores da sua live acessem um portal web moderno interativo para explorar todo o ecossistema de cartas da sua stream sem precisar sobrecarregar o chat da Twitch com comandos de texto

Para garantir segurança total (sem expor seu IP ou dar acesso ao painel de administração), o sistema utiliza a infraestrutura global da **Cloudflare** (via **Cloudflare Quick Tunnels**).

***

### 🚀 O que é o Link Público?

Quando você ativa o Link Público, o bot cria um endereço web seguro com HTTPS (no formato `https://*.trycloudflare.com`) que aponta diretamente para um **portal exclusivo somente-leitura** hospedado na sua própria máquina.

Seus viewers podem abrir o link no computador ou celular e navegar pelas coleções, mercado e ranking em tempo real.

{% hint style="success" %}
**100% Blindado e Seguro:** O Link Público roda em um servidor Express isolado (porta `3001`). Seus espectadores **jamais** terão acesso ao painel de administração, tokens, senhas ou configurações internas.
{% endhint %}

***

### 📱 Páginas e Recursos Disponíveis para os Viewers

O portal público conta com diversas páginas completas e responsivas:

| Página                                        | O que o Viewer encontra?                                                                                                                           |
| --------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **🏠 Início (`index.html`)**                  | Estatísticas da stream em tempo real: total de cartas criadas, pacotes disponíveis, itens no mercado e jogadores ativos.                           |
| **🃏 CartaDex (`cartadex.html`)**             | A enciclopédia completa de cartas do canal. Permite filtrar por tipo, raridade, pacote e buscar cartas específicas.                                |
| **🏪 Marketplace (`marketplace.html`)**       | Vitrine ao vivo com todos os anúncios de cartas e pacotes colocados à venda pelos próprios viewers pelo chat. Exibe ID da venda, vendedor e valor. |
| **🛍️ Loja Rotativa (`loja.html`)**           | Itens especiais vendidos pelo próprio bot com tempo limite e contador regressivo até a próxima rotação.                                            |
| **👥 Jogadores (`usuarios.html`)**            | Lista da comunidade e ranking de colecionadores com nível, XP, pontos e foto de perfil da Twitch.                                                  |
| **👤 Perfil do Colecionador (`perfil.html`)** | Página personalizada do viewer com seu inventário, progresso dos álbuns (cartas obtidas vs faltantes), conquistas e missões.                       |

***

### ⚡ Como Funciona a Conexão (Cloudflare)

O processo é 100% automatizado, sem necessidade de cadastros externos, sem abrir portas no roteador e sem configurar firewall:

{% code overflow="wrap" %}
```
[ Viewers na Web / Celular ]
            │
            ▼ (HTTPS Seguro)
[ Infraestrutura Cloudflare ]
            │
            ▼ (Túnel Criptografado)
[ Servidor Público Local (Porta 3001) ]  ←─── Totalmente isolado do Painel Admin (Porta 3000)
```
{% endcode %}

#### Por que Cloudflare Tunnels?

* **Sem necessidade de conta:** Não exige cadastro, login ou criação de tokens manuais.
* **Sem telas de aviso chatas:** Os viewers entram direto na página sem bloqueios de intermediários.
* **Privacidade total:** Seu endereço IP real fica totalmente oculto.
* **HTTPS nativo:** Conexão rápida com certificado SSL automático.
* **Link dinâmico e seguro:** O link muda a cada ativação, protegendo sua live contra bots e ataques automatizados.

***

### 🛠️ Como Ativar e Usar no Painel

{% stepper %}
{% step %}
#### Ativar o Link Público

1. No aplicativo do **Baralhada**, acesse o menu lateral esquerdo.
2. Na seção **Sistema**, clique em **Link Público** (ícone de globo 🌐).
3. Clique no botão azul **"Gerar e Ligar Link Seguro"**.
4. Aguarde alguns segundos enquanto o túnel Cloudflare é estabelecido.
5. Pronto! O status mudará para **"Túnel Online"** e o link seguro será exibido.
{% endstep %}

{% step %}
#### Compartilhar com a Live

* Clique no link gerado para copiá-lo para a área de transferência.
* Clique em **"Testar Link no Navegador"** para conferir o visual antes de divulgar.
* Envie o link no chat da Twitch ou fixe nos comandos/painéis do seu canal.
{% endstep %}

{% step %}
#### Desligar o Túnel

* Quando encerrar a live, basta clicar no botão vermelho **"Desligar e Fechar Conexão"**.
* O link se tornará inacessível imediatamente, encerrando qualquer conexão externa.
{% endstep %}
{% endstepper %}

***

### 🤖 Integração Automática com o Chat da Twitch

Quando o túnel estiver ativo, o bot no chat responderá automaticamente com o link do site:

| Comando no Chat              | Resposta do Bot                                    |
| ---------------------------- | -------------------------------------------------- |
| `!site`                      | Envia a URL da página inicial do portal.           |
| `!cartadex`                  | Envia o link direto para a enciclopédia de cartas. |
| `!mercado` ou `!marketplace` | Envia o link direto da vitrine do Marketplace.     |
| `!usuarios`                  | Envia o link da lista de jogadores da comunidade.  |

{% hint style="info" %}
Caso o Link Público esteja desligado no painel, o bot responderá no chat avisando educadamente que o site público está desativado no momento.
{% endhint %}

***

### ⚙️ Configurações Avançadas

#### Alterando a Porta do Servidor Local

Por padrão, o servidor público utiliza a porta **`3001`**. Se você já tiver outro programa ou serviço utilizando essa mesma porta no seu computador:

1. Acesse **Link Público** no menu do bot.
2. No campo **"Porta do Servidor Local"**, digite uma nova porta (ex: `3005`).
3. Ligue o túnel. O sistema passará a usar a nova porta automaticamente.

***

### 🔒 Segurança e Boas Práticas

* ✅ **Acesso somente-leitura:** A API do servidor público não permite edições de banco de dados, compras diretas sem validação do chat ou exclusões.
* ✅ **Compras seguras:** Toda transação financeira (pontos/moedas) continua sendo processada estritamente pelo bot no chat da Twitch através de comandos como `!comprar_marketplace <ID>` ou `!comprar <item>`.
* ✅ **Isolamento de processos:** Os processos de tunelamento são encerrados automaticamente ao fechar o bot para evitar portas presas no Windows.
