# Diagnóstico

Uma das funcionalidades mais poderosas "escondidas" no Baralhada Bot é o seu sistema de diagnóstico em tempo real, que captura muito mais do que apenas conversas de chat.

### 🚀 Interceptação de Saída (`stdout/stderr`)

O servidor do bot intercepta automaticamente tudo o que é escrito no terminal do sistema. Isso significa que, se uma biblioteca externa (como a do banco de dados ou da Twitch) gerar um erro ou aviso, o Baralhada o captura e o envia diretamente para o seu **Console** no painel administrativo.

### 🧼 Gerenciamento de Memória

Para evitar que o aplicativo fique lento, o bot mantém apenas os últimos **1000 logs** em memória. Ao reiniciar o app, esses logs temporários são limpos, mantendo apenas os logs permanentes de atividade (economia/transações) que ficam salvos no banco.

{% hint style="info" %}
**Dica Técnica:** Se o bot não estiver respondendo, abra o Console e procure por logs na categoria **TWITCH**. Geralmente, ele dirá exatamente se o problema é senha errada ou falta de conexão.
{% endhint %}

