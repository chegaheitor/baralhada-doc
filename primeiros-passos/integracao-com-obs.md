# 📺 Integração com OBS

## 📺 Overlay e Alertas

O Overlay é o que traz o **Baralhada Bot** visualmente para dentro da sua transmissão. Ele é uma página web transparente que você adiciona como uma **Fonte de Navegador (Browser Source)** no seu software de transmissão (OBS Studio, Streamlabs, etc).

### Funcionamento Técnico

O Overlay é uma página web renderizada de forma transparente. Ele se comunica com o servidor do bot via **WebSockets** (ou requisições constantes) para reagir instantaneamente aos eventos do chat.

### Como Configurar o Overlay

1. No Painel Admin, copie o link do Overlay (Geralmente `http://localhost:PORTA/#/overlay`).
2. No seu OBS, adicione uma nova **Fonte de Navegador**.
3. Cole a URL, defina a resolução (Recomendado: 1920x1080) e marque a opção "Atualizar navegador quando a cena se tornar ativa".

{% hint style="info" %}
Use o campo "Filtro de Croma" no OBS se o fundo não estiver totalmente transparente (embora o bot já envie o fundo transparente por padrão).
{% endhint %}

### Tipos de Alertas Visuais

O overlay exibe automaticamente:

* 📦 **Spawn de Pacotes**: Um alerta visual aparece sempre que um novo pacote cai no chat.
* 🎊 **Abertura de Pacotes**: As cartas sorteadas são reveladas com animações de raridade.
* 🏆 **Conquistas**: Celebração visual de marcos alcançados.
* 🖼️ **Álbum**: Exibição da grade de coleção ao comando `!album`.
* 🤝 **Trocas e Presentes**: Animação detalhando quem enviou e quem recebeu qual item.

{% hint style="info" %}
Você pode testar cada um desses alertas individualmente nestas configurações usando os botões de "Testar Alerta".
{% endhint %}

### Customização dos Alertas

As opções de customização estão divididas entre:

1. **Habilitação**: Ligar ou desligar tipos individuais de alertas (ex: ocultar apenas trocas).
2. **Durações**: Definir quantos segundos cada tipo de alerta fica na tela.
3. **Fotos de Perfil**: Escolha se deseja exibir o avatar da Twitch do usuário nos alertas.
