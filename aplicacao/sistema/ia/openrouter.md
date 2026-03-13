# 🌐 Openrouter

O OpenRouter é um hub (um portal) que te conecta aos melhores e maiores modelos de Inteligência Artificial do mundo (como ChatGPT, Claude e Gemini) através de uma única conta. Ao contrário do Ollama (que roda no seu PC usando sua placa de vídeo), o OpenRouter roda na nuvem, **não consumindo absolutamente nenhum recurso da sua máquina** enquanto você faz stream.

{% hint style="success" %}
A vantagem: Eles possuem **vários modelos que são 100% gratuitos**, rápidos e incrivelmente mais inteligentes que os modelos locais básicos.
{% endhint %}

{% hint style="danger" %}
A maior desvantagem: Os modelos gratuitos podem esgotar rapidamente e ter fila de espera, alem de depender 100% da conexão com a internet.
{% endhint %}

## 🚀 Passo a Passo de Instalação

#### 1. Criando a Conta e a Chave API

1. Acesse [openrouter.ai](https://openrouter.ai).
2. Clique em **Sign In** ou **Sign Up** e faça login (pode usar sua conta do Google, Discord, etc).
3. Após logar, clique na sua foto de perfil no canto superior direito e escolha **Keys** (Chaves).
4. Clique no botão **Create Key**.
5. Dê um nome para a chave (Ex: `BaralhadaBot`) e clique em **Create**.
6. **COPIE A CHAVE QUE APARECERÁ NA TELA!** (Ela começa com `sk-or-v1-`). _Atenção: Você não conseguirá ver essa chave inteira novamente. Se perder, terá que deletá-la e criar outra._

#### 2. Conectando no Baralhada Bot

1. No seu Painel de Controle (Dashboard do Bot), vá em **Sistema > IA**.
2. Ative a chave **IA Ativada**.
3. Selecione o provedor **OpenRouter (Nuvem)**.
4. No campo **OpenRouter Chave (API Key)**, cole aquela chave secreta que você copiou no Passo 1.
5. No campo **Modelo**, você precisará digitar exatamente o código oficial do modelo que quer usar (veja as recomendações abaixo).
6. Salve e clique em **Testar**. Ele deverá te retornar uma saudação no painel vermelho.

***

## 🧠 Modelos Recomendados (Grátis e Pagos)

O OpenRouter tem centenas de IAs. Recomendamos os modelos gratuitos abaixo para não ter dor de cabeça com pagamentos:

### ✨ Modelos `FREE` (Excelentes e Sem Custo)

Se você quer agilidade e zero custo, copie e cole exatamente um destes códigos no campo "Modelo" do seu bot:

| Código (Copie e Cole)                       | Descrição do Modelo                                                                                       |
| ------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| **`google/gemini-2.5-flash:free`**          | 🥇 **Melhor Geral!** Incrivelmente rápido, inteligente, e criativo para inventar bardo de lore e fofocas. |
| **`mistralai/mistral-nemo:free`**           | 🥈 Alternativa se o Gemini estiver lento. Modelos Mistral são famosos pelo excelente português.           |
| **`meta-llama/llama-3.2-3b-instruct:free`** | 🥉 Uma versão muito superior ao `llama3.2:1b` do Ollama, mas rodando sem pesar a sua máquina.             |

{% hint style="info" %}
Modelos gratuitos podem ocasionalmente ter "Rate Limits" (limites de lentidão temporária) se muita gente no mundo estiver usando ao mesmo tempo.
{% endhint %}

### 💸 Modelos `PAGOS` (Alta Inteligência)

Se você tem créditos (R$) no OpenRouter (colocados na aba 'Credits' do site deles) e quer o modelo mais top possível para gerar lore épico sem se preocupar:

<table><thead><tr><th width="262">Código (Copie e Cole)</th><th width="345">Descrição do Modelo</th><th>Custo (aprox)</th></tr></thead><tbody><tr><td><strong><code>openai/o1-mini</code></strong></td><td>Muito rápido, extremamente criativo para narrativas ricas e longas.</td><td>Muito Baixo</td></tr><tr><td><strong><code>anthropic/claude-3.5-haiku</code></strong></td><td>O melhor custo-benefício. Textos super humanos, sarcasmo fino para o mediador de trocas.</td><td>Baixo</td></tr><tr><td><strong><code>openai/gpt-4o-mini</code></strong></td><td>O cérebro padrão do ChatGPT. Excelente para seguir ordens do "Grito de Guerra" à risca.</td><td>Baixo</td></tr></tbody></table>

_(Preços do OpenRouter são debitados frações de centavos por mensagem gerada. Consulte a tabela deles no site)._

***

## ⚠️ Solução de Problemas Comuns

1. **"Erro 401 Unauthorized" / Chave Recusada:**
   * Sua chave API está incorreta ou cortada. Refaça o passo 1 copiando atentamente todo o texto.
2. **"O modelo \[nome\_do\_modelo] não foi encontrado. Verifique seu crédito...":**
   * Você escolheu um modelo pago (sem a tag `:free` no final do nome) e não tem saldo adicionado na sua conta \[openrouter.ai/credits].
   * Troque para o `google/gemini-2.5-flash:free` para resolver isso em 5 segundos, sem pagar nada.
3. **O Bot diz o "Texto Completo", mas corta a mensagem na metade:**
   * Leia sobre **Limites do Token**. No bot por padrão limitamos a fala a 1500 caracteres (ou seja 4 mensagens longas da Twitch juntas). Tente alterar seu prompt da IA no painel adicionando a regra: `"Formule uma frase curta de no máximo 1 parágrafo!"`.

