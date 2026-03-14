# ⚖️ Mediador de Trocas

O **Mediador de Trocas** é o "comentarista" do mercado negro do seu chat. Após dois usuários fecharem uma negociação de cartas oficial usando os comandos do bot, a IA emite uma opinião super sincera (e, na maioria das vezes, sarcástica) sobre quem se deu bem e quem foi passado pra trás no negócio.

***

## 🛠️ Como Funciona?

1. Um espectador propõe uma troca: `!troca @vitima nomedacarta`
2. A "vitima" responde oferecendo algo em troca com `!trocaoferta nomedacarta2`
3. A proposta avança e é aceita com o `!trocasim`
4. O bot processa a troca nos inventários.
5. Se o módulo do Mediador estiver ativo, a Inteligência Artificial é acionada. Ela inspeciona todos os detalhes da Carta A (Ofertada pelo Iniciador) e Carta B (Ofertada pelo Alvo), analisa as estatísticas, coleções e raridades, e decide quem fez o melhor negócio.
6. O bot envia o "veredicto" engraçado em 1 ou 2 frases no chat.

***

## ⚙️ Configurando o Módulo

No Painel de Controle do Baralhada, navegue até **Sistema > IA**. Procure pelo card **"Módulo: Mediador de Trocas"**.

* **Habilitar:** Ligue a chave para ativar a fofoca pós-troca.
* **Prompt (Comando Base):** Defina se o mediador deve ser maldoso, técnico, confuso, torcedor, etc.

***

## 📝 O Prompt e as Variáveis

Neste módulo, enviamos pacotes massivos de texto para a Inteligência Artificial analisar de uma vez só: os atributos inteiros de duas cartas.

#### Exemplo de Prompt (Padrão e Recomendado)

O segredo aqui é proibir a IA de _"falar demais"_ sobre a lore, e focar em ser rápida e cortante:

> Você é o "Mediador de Trocas", um NPC sarcástico e ácido. Analise a troca: {userA} deu "{itemA}" ({detailsA}) p/ {userB}, que deu "{itemB}" ({detailsB}). Sua única tarefa é fazer um comentário curto e sarcástico (MÁX 2 frases) sobre quem levou a melhor ou se a troca foi um desastre. JAMAIS descreva ou liste as propriedades das cartas no texto final. Use as propriedades apenas para sua decisão interna. Use emotes e NÃO use markdown.

#### Exemplo do Chat

_No chat:_ `User1 e User2 finalizaram a troca!`

> _"Nossa, o {User1} acabou de entregar um guerreiro lendário por uma amoeba de água que não causa dano algum do {User2}? Isso me cheira a desespero total ou a uma amizade muito, mas muito suspeita!"_

***

## 💡 Dicas de Uso

* Manter o mediador focado em frases curtas (1 ou 2 sentenças) evita que o módulo analise excessivamente a troca escrevendo textões e cortando a emoção rápida e caótica do momento em que a troca acontece.
* Você pode customizar o Mediador para atuar como personagens famosos do escambo.
