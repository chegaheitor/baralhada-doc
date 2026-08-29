# ✨ Gemini

A API oficial do **Google Gemini** é uma das melhores opções para streamers: além de ser uma das IAs mais rápidas do mundo, ela oferece um **plano gratuito direto e generoso** através do Google AI Studio, sem necessidade inicial de cadastrar cartão de crédito.

Ao rodar na nuvem do Google, ela **não consome absolutamente nenhum recurso do seu computador**, deixando 100% da sua CPU, GPU e memória livres para jogos pesados e o software de stream (OBS Studio).

***

### 🚀 Passo a Passo de Configuração

{% stepper %}
{% step %}
### Criando sua Chave de API Grátis no Google AI Studio

1. Acesse o portal do Google AI Studio: [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey).
2. Faça login com a sua conta do Google.
3. Clique em **Create API key** (Criar Chave de API).
4. Selecione ou crie um projeto do Google Cloud e confirme.
5. **Copie a chave gerada** (começa com `AIzaSy...`).

{% hint style="info" %}
_Dica: Você sempre poderá rever ou copiar essa chave novamente no mesmo painel do AI Studio._
{% endhint %}
{% endstep %}

{% step %}
### Configurando no Baralhada

1. No seu Painel de Controle (Dashboard do Bot), vá na aba lateral em **Sistema > IA**.
2. Ative a chave **IA Ativada**.
3. Selecione o provedor **Gemini (Google Direto)**.
4. No campo **Gemini API Key**, cole a chave que você copiou.
5. No campo **Modelo**, escolha entre as opções sugeridas:
   * `gemini-1.5-flash` (Recomendado: ultra rápido, criativo e gratuito)
   * `gemini-1.5-pro` (Modelo com raciocínio aprofundado)
   * `gemini-2.0-flash-exp` (Versão experimental de nova geração)
6. Clique em **Salvar** e depois em **Testar**.
{% endstep %}
{% endstepper %}

***

### 🧠 Modelos Recomendados (Totalmente Grátis)

O Google AI Studio disponibiliza modelos com limites gratuitos generosos (geralmente até 15 requisições por minuto no plano Free, mais do que suficiente para qualquer live da Twitch).

| Código (Copie e Cole)      | Recomendação                   | Custo no AI Studio            | Descrição e Comportamento                                                                                                                  |
| -------------------------- | ------------------------------ | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **`gemini-1.5-flash`**     | 🥇 **A Melhor Escolha Geral!** | **100% Grátis** (Plano Free)  | Velocidade absurda de resposta (\~0.8s), ótimo entendimento de gírias da Twitch, criatividade para piadas de apostas e narração de duelos. |
| **`gemini-1.5-pro`**       | 🥈 Alta Inteligência           | **100% Grátis** (com limites) | Raciocínio profundo e textos detalhistas. Perfeito para histórias longas no Bardo de Lore (`!lore`) e assistente de criação de cartas.     |
| **`gemini-2.0-flash-exp`** | 🥉 Experimental Nova Geração   | **100% Grátis**               | Versão preview dos novos avanços da família Gemini 2.0 com respostas instantâneas.                                                         |

***

### 💡 Informações sobre Limites e Pagamentos

* **Preciso cadastrar cartão?** Não! O Google AI Studio libera chaves para uso nos modelos padrão sem exigir dados bancários imediatos.
* **Limite de Taxa (RPM):** No plano gratuito do Google, existe um limite de cerca de 15 requisições por minuto. Para um canal na Twitch onde comandos de IA acontecem a cada poucos segundos ou minutos, esse limite é muito confortável.

***

### ⚠️ Solução de Problemas Comuns

1. **"Erro 400 / 403 API Key Invalid" / Chave Recusada:**
   * A sua chave `AIzaSy...` foi colada com caracteres faltando ou o projeto no Google Cloud ainda está inicializando. Aguarde 30 segundos ou gere uma nova chave em [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey).
2. **"O Gemini não retornou nenhum texto (bloqueado por filtros de segurança)":**
   * O Google possui filtros de segurança padrão rígidos para termos de ódio ou assédio. Se o bot gerou uma resposta muito agressiva em um duelo, suavize a instrução no prompt para que a provocação seja esportiva ou engraçada.
3. **Mensagem cortada no chat da Twitch:**
   * O Gemini gosta de escrever de forma rica e completa. Para garantir que ele nunca exceda o limite de caracteres da Twitch, inclua no prompt do painel: _"Responda em no máximo 2 frases curtas"_.
