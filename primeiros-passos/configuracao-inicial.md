# Configuração Inicial

## 🚀 Configuração Inicial

Para que o sistema funcione corretamente, a primeira coisa que você deve fazer ao abrir o programa é configurar as identidades da sua live.

Siga esta ordem de configuração para garantir que tudo funcione de primeira:

### 1. Configurações de Conexão

Vá no menu lateral em **Configurações > Credenciais e Acesso**. Lá você encontrará os campos cruciais:

#### 👤 Canal do Streamer

* **O que é:** O nome do canal onde o bot vai atuar (o seu canal).
* **Como preencher:** Apenas o nome de usuário (ex: `baralhadaStreamer`).

#### 🤖 Credenciais do Bot

O bot precisa de uma "identidade" para falar no chat.

* **Bot Username:** O nome da conta que vai ser o bot. (Pode ser a sua conta principal ou uma conta criada apenas para o bot). ex: `baralhadaBot`
* **Bot OAuth Token:** A "senha" de acesso ao chat. Veja como obter [aqui.](instalacao/oauth-token-bot.md)

{% hint style="warning" %}
Se você mudar a senha da sua conta BOT da Twitch, precisará gerar um novo **OAuth Token** para que o bot volte a funcionar.
{% endhint %}

#### 🔑 Aplicação Dev API (Obrigatório para funções avançadas)

Para que o bot consiga buscar fotos de perfil e verificar informações da API da Twitch.

* **Client ID & Client Secret:** Veja como obter [aqui.](instalacao/aplicacao-dev-twitch.md)

> O Baralhada pode conectar de forma manual apertando o botão de conectar bot, ou você pode ativar a opção de auto-conectar, sempre que o programa abrir, ele irá fazer a conexão de forma automática.

***

### 2. Testando a Conexão

Após salvar as configurações:

1. Clique no botão **"Iniciar Bot"**.
2. Verifique o **Console**. Se aparecer "Conectado", o bot já está lendo seu chat!

<pre><code>Bot<a data-footnote-ref href="#user-content-fn-1"> conectado com sucesso ao canal (BaralhadaStreamer)</a>
</code></pre>

Quando o bot conecta, ele envia uma mensagem no chat:

```
🚀 Sistema TCG Online! Preparem-se, caçadores de cartas! 🃏
```

Isso confirma que tudo está funcionando corretamente.

***

### 3. Próximos Passos

Com o bot conectado, você pode começar a:

* Criar suas primeiras **Cartas e Pacotes**.
* Configurar quanto cada espectador ganha em **Economia e Pontos**.
* Adicionar o **Overlay no OBS**.

{% hint style="info" %}
Sempre que alterar uma configuração de conexão, recomendamos desligar e ligar o bot novamente para garantir que as novas credenciais foram aplicadas.
{% endhint %}

***

## ⁉ Solução de Problemas

<details>

<summary>Bot não conecta</summary>

* Verifique se o token OAuth está correto e atual
* Confirme se o nome do canal está sem `#` ou `@`
* Gere um novo token em [https://twitchtokengenerator.com/](https://twitchtokengenerator.com/)

</details>

<details>

<summary>"No response from Twitch" no log</summary>

* Sinal de instabilidade da conexão IRC do Twitch — isso é normal e o bot tenta reconectar automaticamente

</details>

<details>

<summary>Porta já em uso</summary>

* Mude a porta em Configurações (ex: `3001`) e reinicie o app

</details>

[^1]: 
