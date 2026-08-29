# 🌀 ChatGPT

Usar a API direta da **OpenAI** conecta o seu Baralhada diretamente aos servidores oficiais do **ChatGPT**. Essa é a escolha ideal para quem busca respostas ultra rápidas, altíssima estabilidade e total obediência às regras de personalidade do chat.

Ao rodar na nuvem oficial da OpenAI, o bot **não consome memória RAM, processador nem placa de vídeo do seu computador**, deixando 100% dos recursos livres para a sua live e seus jogos.

***

### 🚀 Passo a Passo de Configuração

{% stepper %}
{% step %}
### Criando sua Chave de API na OpenAI

1. Acesse o portal oficial de desenvolvedores da OpenAI: [platform.openai.com](https://platform.openai.com).
2. Faça login com sua conta da OpenAI (a mesma conta que você usa no ChatGPT).
3. No menu lateral esquerdo, vá em **API Keys** (ou acesse [platform.openai.com/api-keys](https://platform.openai.com/api-keys)).
4. Clique no botão **+ Create new secret key**.
5. Dê um nome para a chave (Ex: `Baralhada Bot`) e confirme.
6. **Copie a chave imediatamente** (ela começa com `sk-proj-...`). _Atenção: A chave só é mostrada uma única vez._

{% hint style="warning" %}
_Atenção: Por motivos de segurança da OpenAI, essa chave só é exibida uma única vez. Se você fechar a janela sem copiar, terá que criar outra._
{% endhint %}
{% endstep %}

{% step %}
### Adicionando Saldo/Créditos (Billing)

1. No menu lateral da OpenAI, vá em **Settings > Billing** (ou [platform.openai.com/settings/organization/billing](https://platform.openai.com/settings/organization/billing)).
2. Clique em **Add payment details** e adicione um cartão de crédito.
3. Faça uma recarga inicial mínima (ex: $5 dólares, que costuma durar centenas de milhares de mensagens geradas no modelo `gpt-4o-mini`).

{% hint style="info" %}
**Atenção sobre o ChatGPT Plus:** A assinatura mensal de R$ 100/mês do ChatGPT Plus **não inclui** o uso da API de desenvolvedor. A API opera em um sistema pré-pago separado.
{% endhint %}
{% endstep %}

{% step %}
### Configurando no Baralhada

1. No seu Painel de Controle (Dashboard do Bot), vá na aba lateral em **Sistema > IA**.
2. Ative a chave **IA Ativada**.
3. Selecione o provedor **ChatGPT (OpenAI Direto)**.
4. No campo **OpenAI API Key**, cole a sua chave `sk-proj-...`.
5. No campo **Modelo**, você pode digitar o modelo ou clicar nas sugestões rápidas:
   * `gpt-4o-mini` (Recomendado: ultra rápido, inteligente e super econômico)
   * `gpt-4o` (Modelo topo de linha mais avançado)
   * `gpt-3.5-turbo` (Modelo clássico)
6. Clique em **Salvar** e depois em **Testar**.
{% endstep %}
{% endstepper %}

***

### 🧠 Modelos Recomendados e Custos

A OpenAI disponibiliza diversos modelos. Para o bot de cartas da Twitch, recomendamos os modelos da tabela abaixo:

<table><thead><tr><th width="151">Código (Copie e Cole)</th><th width="157">Recomendação</th><th width="163">Custo Estimado</th><th>Descrição e Comportamento</th></tr></thead><tbody><tr><td><strong><code>gpt-4o-mini</code></strong></td><td>🥇 <strong>A Melhor Escolha!</strong></td><td><em>Fração de Centavos</em> (Ultra Barato)</td><td>Incrivelmente veloz (resposta em ~1s), inteligência de sobra para piadas, sarcasmo e narração de duelos. Ideal para lives diárias.</td></tr><tr><td><strong><code>gpt-4o</code></strong></td><td>🥈 Alta Complexidade</td><td><em>Médio</em></td><td>O modelo mais inteligente e refinado da OpenAI. Recomendado se você busca contos de RPG e lores extremamente elaboradas no <code>!lore</code>.</td></tr><tr><td><strong><code>gpt-3.5-turbo</code></strong></td><td>🥉 Clássico</td><td><em>Baixo</em></td><td>Modelo tradicional. Rápido e objetivo, embora menos criativo que o <code>gpt-4o-mini</code>.</td></tr></tbody></table>

***

### ⚠️ Solução de Problemas Comuns

1. **"Erro 401 Unauthorized" / Chave Inválida:**
   * Sua chave de API foi copiada incorretamente ou foi revogada no painel da OpenAI. Crie uma nova chave em `platform.openai.com/api-keys` e cole novamente no painel do bot.
2. **"Erro 429 - Insufficient Quota" / Limite de Cota:**
   * Você não possui saldo pré-pago ativo na conta da OpenAI. Acesse `platform.openai.com/settings/organization/billing` e adicione $5 dólares de saldo para liberar as requisições.
3. **"Timeout na resposta da IA":**
   * Se o bot demorar muito para responder em horários de pico, aumente o campo **Tempo Limite da IA (Timeout)** nas configurações de IA de 30 para 60 segundos.
4. **Respostas cortadas no Chat da Twitch:**
   * O chat da Twitch possui limites por mensagem. Adicione ao seu prompt no painel uma instrução explícita como: _"Mantenha as respostas curtas com no máximo 2 a 3 frases"_.
