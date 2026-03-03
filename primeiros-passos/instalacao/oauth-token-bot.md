# 🔑 Oauth Token Bot

## 🤖 Como obter o Token OAuth do Bot

Para que o bot possa ler o chat e enviar mensagens, ele precisa de um **Token OAuth**. Este token funciona como a "senha" do bot para o chat da Twitch.

Siga os passos abaixo usando a ferramenta recomendada:

### 1. Acesse o Twitch Token Generator

Vá para o site [TWITCHTOKENGENERATOR.COM](https://twitchtokengenerator.com/).

### 2. Selecione o Tipo de Token

1. No menu principal, procure por **"Bot Chat Token"** ou use o gerador customizado.
2. Certifique-se de estar logado na Twitch com a **CONTA DO BOT** (não a sua pessoal, a menos que você queira que sua conta pessoal seja o próprio bot).

### 3. Configure as Permissões (Scopes)

Para o Baralhada Bot funcionar, você **DEVE** selecionar os seguintes itens (scopes):

#### ✅ OBRIGATÓRIOS (Sem eles o bot não funciona):

* `chat:read`: Permite que o bot leia as mensagens e comandos (como `!claim`).
* `chat:edit`: Permite que o bot responda e envie mensagens no chat.
* `user:write:chat`: (Novo) Permite enviar mensagens via API moderna da Twitch.
* `channel:bot`: Identifica a conta oficialmente como um Bot para a Twitch.
* `user:bot`: Permite que a conta atue como um bot.

#### 🌟 RECOMENDADOS (Para melhor funcionamento):

* `channel:moderate`: Permite que o bot execute ações de moderação (útil para comandos de moderação futuros).
* `whispers:read` e `user:manage:whispers`: Permite que o bot responda via sussurro se configurado.
* **`channel:read:redemptions`**: Permite que o bot interaja quando alguém resgata um item na loja de pontos da Twitch (sem digitar nada no chat).

### 4. Gere e Autorize

1. Clique no botão **"Generate Token"**.
2. Uma janela da Twitch aparecerá pedindo autorização. Clique em **Autorizar**.

### 5. Copie o Access Token

1. O site mostrará o campo **"Access Token"**.
2. Ele se parece com algo assim: `a1b2c3d4e5f6g7h8i9j0...`
3. **Copie o código completo**.

{% hint style="warning" %}
**\[IMPORTANTE]** Nunca mostre este token em live ou para outras pessoas! Ele dá acesso total ao chat do seu canal. Se vazar, gere um novo imediatamente no site e atualize no bot.
{% endhint %}

### 6. Configure no Baralhada Bot

1. Abra o painel administrativo do bot.
2. Vá em **Configurações** > **Twitch e Conexão**.
3. Cole o token no campo **Bot OAuth Token**.
4. Salve as configurações.

Pronto! Agora seu bot tem "permissão de fala" no seu chat. 💬
