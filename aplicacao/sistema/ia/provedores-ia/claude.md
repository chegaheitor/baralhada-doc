# ✴️ Claude

Conectar o Baralhada diretamente à API oficial da **Anthropic** traz a inteligência e o consagrado talento literário da família **Claude**. O Claude é reconhecido mundialmente como o melhor modelo para diálogos humanos, interpretação de personagens, piadas orgânicas e sarcasmo de alta qualidade.

Por operar diretamente na nuvem da Anthropic, **ele não pesa na memória, no processador ou na GPU do seu computador**, garantindo performance máxima para seu jogo e transmissão de stream.

***

### 🚀 Passo a Passo de Configuração

{% stepper %}
{% step %}
### Criando sua Chave de API na Anthropic

1. Acesse o console oficial da Anthropic: [console.anthropic.com](https://console.anthropic.com).
2. Crie uma conta ou faça login.
3. No menu superior ou lateral, clique em **API Keys** (ou acesse [console.anthropic.com/settings/keys](https://console.anthropic.com/settings/keys)).
4. Clique em **+ Create Key**.
5. Dê um nome (Ex: `Baralhada Bot`) e clique em **Create Key**.
6. **Copie a chave imediatamente** (ela começa com `sk-ant-api03-...`).

{% hint style="warning" %}
_Atenção: A chave só aparece uma vez no momento da criação._
{% endhint %}
{% endstep %}

{% step %}
### Adicionando Créditos (Plans & Billing)

1. No console da Anthropic, vá na seção **Settings > Plans & Billing** (ou [console.anthropic.com/settings/plans](https://console.anthropic.com/settings/plans)).
2. Clique em **Claim Free Credits** (se houver créditos iniciais de teste disponíveis) ou cadastre seu cartão em **Add Credits**.
3. Uma recarga de $5 dólares é suficiente para dezenas de milhares de interações com o modelo Haiku.

{% hint style="info" %}
**Atenção sobre a assinatura Claude Pro:** Assim como na OpenAI, a assinatura do Claude Pro para uso no navegador **não dá créditos para a API**. O console de desenvolvedor funciona com créditos pré-pagos à parte.
{% endhint %}
{% endstep %}

{% step %}
### Configurando no Baralhada

1. No seu Painel de Controle (Dashboard do Bot), vá na aba lateral em **Sistema > IA**.
2. Ative a chave **IA Ativada**.
3. Selecione o provedor **Claude (Anthropic Direto)**.
4. No campo **Anthropic API Key**, cole a sua chave `sk-ant-api03-...`.
5. No campo **Modelo**, escolha ou digite um dos modelos disponíveis:
   * `claude-3-5-haiku-20241022` (Recomendado: extremamente veloz e excelente custo-benefício)
   * `claude-3-5-sonnet-20241022` (O modelo mais inteligente para histórias complexas e RPG)
   * `claude-3-opus-20240229` (Modelo premium clássico)
6. Clique em **Salvar** e depois em **Testar**.
{% endstep %}
{% endstepper %}

***

### 🧠 Modelos Recomendados e Custos

A Anthropic possui 3 famílias principais de modelos. Para uso em chats de Twitch, recomendamos:

<table><thead><tr><th width="181">Código (Copie e Cole)</th><th width="176">Recomendação</th><th width="120">Custo Estimado</th><th>Descrição e Personalidade</th></tr></thead><tbody><tr><td><strong><code>claude-3-5-haiku-20241022</code></strong></td><td>🥇 <strong>A Melhor Escolha!</strong></td><td><em>Super Baixo</em></td><td>Velocidade relâmpago, excelente custo-benefício e escrita surpreendentemente espirituosa para fofocas do chat e o Cobrador Sarcástico.</td></tr><tr><td><strong><code>claude-3-5-sonnet-20241022</code></strong></td><td>🥈 Alta Literatura</td><td><em>Médio</em></td><td>O modelo mais inteligente do mundo para interpretação de RPG e lore. Perfeito para o Bardo da Lore (<code>!lore</code>) e descrições profundas de cartas.</td></tr><tr><td><strong><code>claude-3-opus-20240229</code></strong></td><td>🥉 Premium</td><td><em>Mais Alto</em></td><td>Modelo denso e detalhista para projetos que exigem raciocínio complexo.</td></tr></tbody></table>

***

### ⚠️ Solução de Problemas Comuns

1. **"anthropic-workspace-id is required when authenticating with an identity-linked API key":**
   * **O que significa:** A sua chave de API foi gerada no perfil pessoal/identidade da conta, em vez de ser gerada diretamente dentro de um Workspace da Anthropic.
   * **Como resolver (Opção 1 - Recomendada):** Acesse `console.anthropic.com`, selecione seu Workspace no menu (ex: "Default") e gere a chave dentro da aba **API Keys desse Workspace**. Chaves criadas dentro do Workspace funcionam direto sem precisar de Workspace ID.
   * **Como resolver (Opção 2):** Acesse `console.anthropic.com/settings/workspaces`, copie o ID do seu Workspace (ou pegue o código na URL do seu navegador após `/workspaces/`) e cole no campo **Anthropic Workspace ID** no painel do Baralhada Bot.
2. **"Erro 401 Unauthorized" / Chave Recusada:**
   * A sua chave `sk-ant-api03-...` foi copiada com espaços extras ou está incorreta. Acesse `console.anthropic.com/settings/keys` e gere uma nova chave.
3. **"Erro 429 - Credit Balance is too low" / Saldo Insuficiente:**
   * Sua conta está sem saldo pré-pago no console da Anthropic. Vá em `console.anthropic.com/settings/plans` e adicione créditos para ativar a API.
4. **Demora na Resposta ou Timeout:**
   * O modelo `claude-3-5-sonnet` pode levar alguns segundos adicionais para gerar lores longas. Mantenha o **Timeout** em 30 ou 45 segundos no painel.
5. **Regras de Moderação e Linguagem:**
   * O Claude possui diretrizes de segurança éticas sólidas. Em provocações de duelo (`!atacar`), certifique-se de que o prompt instrua o bot a focar em _humor, rivalidade esportiva e RPG_, evitando termos ofensivos reais.
