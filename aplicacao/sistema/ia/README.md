# 🧠 IA

Bem-vindo ao módulo de Inteligência Artificial do Baralhada! Transforme o seu chat da Twitch em uma experiência viva, narrativa e cheia de fofoca.

## 🤖 O que é a Integração de IA do Bot?

Diferente de comandos tradicionais que sempre respondem a mesma frase gravada, o **Baralhada** possui integração com Modelos de Linguagem Grande (LLMs, como o ChatGPT).

Isso significa que o bot "ganha vida". Quando um evento importante acontece (uma carta é ganhada, um duelo épico), o bot não apenas anuncia o fato; ele **cria uma narrativa única na hora** baseada no contexto do que aconteceu. Ele lê os atributos da carta, a situação do jogador, mistura tudo com as regras que você definiu, e gera uma mensagem que nunca será idêntica duas vezes.

## ⚙️ Como a IA Funciona no Fundo?

Para usar a IA, o bot age como um intermediário. O fluxo é simples:

{% stepper %}
{% step %}
### Gatilho

Alguém digita um comando ou ganha um prêmio no chat.
{% endstep %}

{% step %}
### **Coleta de Dados**

O bot pega todas as informações do banco de dados (Lore da carta, pontos de ataque, nome do usuário, etc).
{% endstep %}

{% step %}
### **O Prompt**

O bot junta as informações estruturadas de cima com o _Prompt Base_ (as instruções de como o Bot deve agir, que você escreve no Painel).
{% endstep %}

{% step %}
### **O Motor (Provedor)**

O bot envia esse pacotão de texto para um "Motor" de Inteligência Artificial.
{% endstep %}

{% step %}
### **A Resposta**

O motor pensa, cria o texto final ("Ah, mero mortal, me invocou?"), devolve pro bot, e o bot imprime no chat do seu canal.
{% endstep %}
{% endstepper %}

## 🔌 Escolhendo o seu "Motor: Nuvem vs Local"

O bot precisa de um motor para "pensar". O Baralhada suporta 5 motores líderes de mercado, tanto em nuvem direta, hub ou processamento 100% local:

####

Conecte aos modelos da Anthropic como `claude-3-5-haiku` e `claude-3-5-sonnet`.

* **Vantagens:** Textos extremamente naturais, narrativa rica e ótimo sarcasmo.
* 👉 Ver Guia Completo do Claude

#### 🔵 Google Gemini (Nuvem Direta)

Conecte diretamente pelo Google AI Studio para usar modelos como `gemini-1.5-flash` e `gemini-2.0-flash-exp`.

* **Vantagens:** Plano gratuito generoso, velocidade ultrarrápida e criatividade.
* 👉 Ver Guia Completo do Gemin



<table data-view="cards" data-search="true"><thead><tr><th></th><th></th><th></th><th></th><th data-type="content-ref"></th><th data-hidden data-card-cover data-type="image">Cover image</th></tr></thead><tbody><tr><td><h4>💻 Local (Ollama)</h4></td><td>Sua própria Placa de Vídeo / Processador fará o trabalho de pensar e gerar o texto.</td><td><p></p><div data-gb-custom-block data-tag="hint" data-style="success" class="hint hint-success"><p>100% Gratuito sempre. Sem filas. Totalmente privado. Não depende de serviço externo cair</p></div></td><td><p></p><div data-gb-custom-block data-tag="hint" data-style="danger" class="hint hint-danger"><p>Vai sugar o processamento do seu PC. Se não tiver uma boa placa de vídeo ou memória RAM livre sobrando além da que a OBS + Jogo usam, o gerador ficará lento.</p></div></td><td><a href="provedores-ia/ollama.md">ollama.md</a></td><td><a href="https://www.homedock.cloud/_astro/ollama-logo-on-black-sand.C8U_3a1n_1N2Jl8.webp">https://www.homedock.cloud/_astro/ollama-logo-on-black-sand.C8U_3a1n_1N2Jl8.webp</a></td></tr><tr><td><h4>☁️ Nuvem (OpenRouter)</h4></td><td>Seu bot se conecta pela internet a supercomputadores de empresas gigantes (Google, Meta, OpenAI).</td><td><p></p><div data-gb-custom-block data-tag="hint" data-style="success" class="hint hint-success"><p>Não usa o processamento do seu PC. Tem acesso às IAs mais inteligentes do mundo. Existem planos <strong>totalmente gratuitos</strong>.</p></div></td><td><p></p><div data-gb-custom-block data-tag="hint" data-style="danger" class="hint hint-danger"><p>Depende de internet e os servidores gratuitos podem ter fila de espera às vezes.</p></div></td><td><a href="provedores-ia/openrouter.md">openrouter.md</a></td><td><a href="https://picperf.io/https://laravelnews.s3.amazonaws.com/featured-images/laravel-openrouter.png">https://picperf.io/https://laravelnews.s3.amazonaws.com/featured-images/laravel-openrouter.png</a></td></tr><tr><td><h4>🌀 ChatGPT / OpenAI (Nuvem Direta)</h4></td><td>Conecte diretamente à sua conta de desenvolvedor da OpenAI para usar modelos rápidos e econômicos como <code>gpt-4o-mini</code> e <code>gpt-4o</code>.</td><td><p></p><div data-gb-custom-block data-tag="hint" data-style="success" class="hint hint-success"><p>Oferece respostas quase instantâneas e altíssima estabilidade, com excelente obediência a regras estritas de formato e limites de caracteres do chat. </p></div></td><td><p></p><p></p><div data-gb-custom-block data-tag="hint" data-style="danger" class="hint hint-danger"><p>Exige a inserção de saldo ou créditos pré-pagos na plataforma da OpenAI, já que a assinatura padrão do ChatGPT Plus não é compartilhada com a API.</p></div></td><td><a href="provedores-ia/chatgpt.md">chatgpt.md</a></td><td><a href="https://backendless.com/wp-content/uploads/2023/07/ChatGPT-Logo.png">https://backendless.com/wp-content/uploads/2023/07/ChatGPT-Logo.png</a></td></tr><tr><td><h4>✴️ Claude / Anthropic (Nuvem Direta)</h4></td><td>Conexão oficial direta com a API da Anthropic para usar os modelos <code>claude-3-5-haiku</code> e <code>claude-3-5-sonnet</code>.</td><td></td><td><p></p><div data-gb-custom-block data-tag="hint" data-style="success" class="hint hint-success"><p>Destaca-se por uma escrita mais humana, rica e imersiva para narrativas e RPG, sendo perfeito para o baralhada.</p></div><p></p><div data-gb-custom-block data-tag="hint" data-style="danger" class="hint hint-danger"><p>Necessita de cadastro e créditos pré-pagos no console da Anthropic, sem dispor de uma cota gratuita contínua para uso regular.</p></div></td><td><a href="provedores-ia/claude.md">claude.md</a></td><td><a href="https://sm.ign.com/ign_br/screenshot/default/68c469d23594abeb9ab6ee48-og-claude-generic_taey.jpg">https://sm.ign.com/ign_br/screenshot/default/68c469d23594abeb9ab6ee48-og-claude-generic_taey.jpg</a></td></tr><tr><td><h4>✨ Google Gemini (Nuvem Direta)</h4></td><td>Conexão oficial pelo Google AI Studio para usar modelos como <code>gemini-1.5-flash</code> e <code>gemini-2.0-flash-exp</code>.</td><td></td><td><p></p><div data-gb-custom-block data-tag="hint" data-style="success" class="hint hint-success"><p>Conta com um plano gratuito generoso e direto pelo AI Studio, entregando velocidade ultrarrápida de resposta sem travar a live e excelente criatividade para criação de lore de cartas e piadas.</p></div><p></p><div data-gb-custom-block data-tag="hint" data-style="danger" class="hint hint-danger"><p>Os filtros de moderação automáticos do Google podem eventualmente bloquear palavras em duelos com provocações muito agressivas.</p></div></td><td><a href="provedores-ia/gemini.md">gemini.md</a></td><td><a href="https://t2.tudocdn.net/765699?w=1200&#x26;h=1200">https://t2.tudocdn.net/765699?w=1200&#x26;h=1200</a></td></tr></tbody></table>

***

## 📜 Funcionalidades e Módulos da IA

Agora que você já tem o motor ligado, é só ativar as atrações do parque! O Baralhada possui módulos específicos onde a Inteligência Artificial brilha forte.

Para ativar e configurar os _"Prompts"_ (Instruções de Personalidade) de cada um, acesse seu painel interno em **Sistema > IA**.

Navegue abaixo para entender como cada módulo mágico funciona e pegar dicas de Prompts incríveis:

* 🎭 [**Apresentação de Carta**](funcionalidades/apresentacao-de-carta.md)**:** As cartas falam! Sinta a força delas quando elas droparem do pacote.&#x20;
* 🗣️ [**Comando !fala**](funcionalidades/comando-fala.md)**:** Permite que os jogadores conversem diretamente com suas próprias cartas.
* 🧠 [**Assistente de Criação**](funcionalidades/assistente-de-criacao.md)**:** A varinha mágica que rascunha lores e nomes diretamente na criação das cartas.
* 😈 [**Cobrador Sarcástico**](funcionalidades/cobrador-sarcastico.md)**:** Um banqueiro maldoso que tira sarro de quem chora por perder pontos em apostas.
* 🧥 [**Espião Secreto**](funcionalidades/espiao-secreto.md)**:** O informante que vende charadas misteriosas sobre quais cartas faltam para o seu álbum.&#x20;
* ⚔️ [**Grito de Guerra**](funcionalidades/grito-de-guerra.md)**:** Antes do sangue rolar nos duelos, os combatentes provocam e o locutor hypa a batalha.&#x20;
* 📰 [**Jornalista Fofoqueiro**](funcionalidades/jornalista-fofoqueiro.md)**:** O noticiário fofoqueiro da sua live que expõe os gastões e todas as brigas da sessão.&#x20;
* 🎵 [**Bardo de Lore**](funcionalidades/bardo-da-lore.md)**:** Um contador clássico de histórias de RPG na fogueira.
* ⚖️ [**Mediador de Trocas**](funcionalidades/mediador-de-trocas.md)**:** Deixe a IA julgar de forma sarcástica quem saiu perdendo numa troca de cartas.

***

## 🛡️ Dicas de Segurança e Estabilidade

1. **A Regra dos Limites:** Lembre-se, o chat da Twitch aceita mensagens de até 500 caracteres. Nós configuramos o bot para tolerar e "fatiar" respostas da IA em até 4 mensagens consecutivas. **Sempre ordene no seu Prompt para que a Inteligência seja breve!** Se ela discursar demais e passar disso, o bot cortará a história.
2. **Sempre haverá erro:** IAs demoram pra responder, ficam confusas ou serviços caem. Relaxa, o bot possui `try-catch` em tudo; se a sua internet falhar e ela não gerar a mensagem, o bot prossegue normalmente com a funcionalidade. Exemplo: Caso o bot não gere o Grito de Guerra de cada carta, o duelo acontece do mesmo jeito, manual e sem a IA
3. **Não sabe o que colocar no prompt?** Use as recomendações que disponibilizamos nos guias de cada módulo linkados acima! Nós testamos muito eles.
