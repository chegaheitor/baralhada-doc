# 🖊️ Assistente de Criação

O **Assistente de Criação** foi desenhado para facilitar e impulsionar a criatividade de quem administra as cartas no Painel de Controle (Dashboard). Em vez de gastar horas quebrando a cabeça para bolar descrições imersivas de fantasia, você usa a IA para preencher os campos com base num pequeno rascunho.

***

## 🛠️ Como Funciona?

1. O Administrador acessa o Painel de Controle e clica em **Cartas > Adicionar Carta** ou tenta editar uma existente.
2. Acima de toda caixa de texto de descrição, existe um pequeno botão de "Gerar Texto".
3. O administrador escolhe os atributos mínimos daquela carta, ou apenas digita algumas palavras soltas (Ex: "urso de fogo, muito furioso").
4. Ao clicar na varinha mágica da Descrição ou Nome, a inteligência lê o Prompt Base (as regras gerais de mundo do jogo) e envia um pedido de criatividade.
5. Em segundos, o sistema sobrescreve a caixa com nomes e descrições ricamente detalhados.

***

## ⚙️ Configurando o Módulo

No Painel de Controle, navegue até **Sistema > IA**. Procure pelo card **"Assistente de Criação"**.

* **Habilitar:** Ative para permitir a varinha mágica na tela Admin.
* **Prompt (Comando Base):** Este é o mais importante de todos. Aqui você ditará a "Bíblia" do seu universo do jogo, como a IA deve enxergar as classes e elementos.

***

### 📝 O Prompt Geral da Criação

No Assistente de Criação, o ideal é focar não em variáveis específicas da troca ou luta, mas sim focar na **tonalidade** global do projeto.

#### Exemplo de Prompt (Criação de Nome)

> _Você é um assistente criativo para um jogo de cartas colecionáveis. Responda APENAS com o nome sugerido, sem explicações ou texto adicional. Crie um nome criativo e curto para uma carta de raridade {rarity}, tipo {type}{type2} e da coleção {collection}. Instruções adicionais: {instructions}. NÃO usar markdown._

#### Exemplo de Prompt (Criação de Descrição)

> _Você é um assistente criativo para um jogo de cartas colecionáveis. Responda APENAS com a descrição, sem textos introdutórios tipo "Aqui está a descrição". Crie ou melhore a descrição de uma carta chamada {name} de raridade {rarity}, tipo {type}{type2} e da coleção {collection}. Atributos: HP {hp}, ATK {attack}, DEF {defense}. Descrição atual: {currentDescription}. Instruções do usuário: {instructions}. Seja breve e imersivo. NÃO usar markdown._

***

### 💡 Dicas de Uso

* Se o jogo de cartas é focado em ficção científica (Naves Espaciais, Cyberpunk), no prompt diga: _"Você é um assistente criativo para Cards Sci-Fi Estelar cyberpunk."_
* Este assistente serve só para os **Admins** e o painel, viewers não têm acesso a essa inteligência artificial, então não precisa se preocupar com limites de gastos se usar OpenRouter pago.
