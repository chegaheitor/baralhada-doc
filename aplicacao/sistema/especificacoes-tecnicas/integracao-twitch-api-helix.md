# 🟣 Integração Twitch API (Helix)

O Baralhada vai além de um bot de chat comum ao utilizar a **Twitch Helix API**. Essa integração permite que o bot tenha um visual muito mais rico, buscando fotos de perfil e informações detalhadas dos usuários em tempo real.

### 🔑 Client ID e Client Secret

Para que o bot possa "conversar" com a API oficial da Twitch, você precisa configurar o `Client ID` e o `Client Secret` em **Sistema > Configurações**.

* **App Access Tokens:** O bot gerencia automaticamente o ciclo de vida dos tokens de acesso. Se um token expirar, o bot detecta o erro e renova a credencial sem que você precise fazer nada.

### 🖼️ Proxy de Avatares

O Baralhada possui uma rota inteligente (`/api/twitch/avatar/:login`) que funciona como um redirecionador.

* **Como funciona:** Quando você abre a página de usuários, o bot pergunta à Twitch qual a foto de perfil atual daquele espectador.
* **Fallback:** Se o usuário não tiver foto ou a API falhar, o bot gera automaticamente um avatar elegante com as iniciais do nome do usuário em um fundo colorido, garantindo que a sua interface nunca fique com imagens quebradas.

### 💬 Inteligência no Envio de Mensagens

A Twitch possui limites de caracteres por mensagem (aproximadamente 500). O Baralhada possui um sistema de **Splitting Automático**:

1. Se uma mensagem (como uma lista de cartas ou conquistas) for muito longa, o bot a divide em partes.
2. Ele procura por espaços vazios ou quebras de linha para não cortar palavras ao meio.
3. Envia as partes com um pequeno atraso entre elas para evitar que você seja banido por "flood".

{% hint style="danger" %}
**Segurança:** Nunca mostre seu Client Secret em live. Se precisar configurar o bot durante a transmissão, use o recurso de "Esconder Token" ou mude a cena do OBS.
{% endhint %}
