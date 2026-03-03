# 🛠️ Configurações

## ⚙️ O que são as Configurações

Divididas em módulos, as configurações permitem que você defina desde as credenciais da API da Twitch até as regras de segurança e economia.

{% hint style="info" %}
NUNCA mostre sua página de configurações em live. Seus tokens são informações sigilosas e não devem ser vazadas!
{% endhint %}

## 🔑 Credenciais da Twitch

* **Impacto**: Sem estas chaves, o bot não pode ler o chat nem saber quem está assistindo.
* **Dica**: Siga o guia passo a passo de "[Configuração Inicial](../../primeiros-passos/configuracao-inicial.md)" para gerar suas chaves no portal de desenvolvedores da Twitch.

{% hint style="danger" %}
**Importante:** Qualquer alteração nas credenciais de API exige que o bot seja REINICIADO para que a conexão seja restabelecida.
{% endhint %}

<table><thead><tr><th width="233">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Usuário do Bot</strong></td><td>Username da conta bot (ex: <code>chegabotTCG</code>)</td></tr><tr><td><strong>Token OAuth</strong></td><td>Token de autenticação gerado em <a href="https://twitchtokengenerator.com/">https://twitchtokengenerator.com/</a></td></tr><tr><td><strong>Nome do Canal</strong></td><td>Seu canal (sem <code>@</code> ou <code>#</code>)</td></tr><tr><td><strong>Twitch Client ID</strong></td><td>Da aplicação em <a href="https://dev.twitch.tv/console/apps">https://dev.twitch.tv/console/apps</a></td></tr><tr><td><strong>Twitch Client Secret</strong></td><td>Da aplicação em <a href="https://dev.twitch.tv/console/apps">https://dev.twitch.tv/console/apps</a></td></tr></tbody></table>

## 🌐 Porta do Servidor

O sistema opera localmente (`localhost`), utilizando uma porta específica para comunicação interna e exibição do painel.

* **Porta Padrão**: O bot utiliza a porta `3000` por padrão.
* **Conflitos**: Caso você já possua outro programa ou serviço (como servidores web ou outros bots) utilizando a porta `3000`, ocorrerá um erro de inicialização.
* **Ajuste**: Se houver interferência, você pode alterar o número da porta nas configurações para qualquer valor disponível (ex: `3001`, `8080`).

{% hint style="warning" %}
**Interferência de Rede:** Se o painel administrativo não carregar, verifique se a porta escolhida não está sendo bloqueada pelo seu Firewall ou se outro software já a reservou.
{% endhint %}

## 📡 Teste de Conexão

Após preencher os dados, use o botão **"Conectar Bot"** no Dashboard ou no Console. Se todos os dados estiverem corretos, o status mudará para `Conectado` e o bot enviará uma mensagem de boas-vindas no chat.

{% hint style="warning" %}
Se você mudar a senha da sua conta da Twitch, precisará gerar um novo **OAuth Token** para que o bot volte a funcionar.
{% endhint %}
