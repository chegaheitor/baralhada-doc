# 🏗️ Arquitetura e Conectividade

O Baralhada Bot é uma aplicação híbrida que combina o poder do **Electron** para a interface desktop com a flexibilidade de um servidor **Node.js/Express** para gerenciar a lógica do bot e a API.

### 🔌 O Servidor Interno

Ao abrir o aplicativo, um servidor web é iniciado localmente. Este servidor é responsável por:

* Gerenciar a conexão com a Twitch via TMI.js.
* Processar comandos e mensagens do chat.
* Fornecer dados para o Painel Administrativo e para os Overlays.

### 📁 Servindo Arquivos (Static Assets)

Todas as imagens de cartas e pacotes que você sobe (`uploads`) são servidas diretamente pelo motor do Express. Elas ficam armazenadas na sua pasta de Documentos para garantir que, mesmo que você atualize o aplicativo, suas imagens nunca sejam perdidas.

{% hint style="info" %}
Essa arquitetura garante que o Baralhada funcione de forma independente, sem depender de servidores externos lentos, garantindo a menor latência possível para os seus Overlays.
{% endhint %}
