# 🎰 Cobrador Sarcástico

O **Cobrador Sarcástico** é um personagem automatizado da IA, desenhado para zombar (ou parabenizar exageradamente) quem se aventura e perde o limite no cassino das cartas, usando o comando de aposta de pontos.

***

## 🛠️ Como Funciona?

1. O Bot roda um comando econômico `!apostar <valor>`.
2. A mecânica de cassino decide matematicamente a sorte e calcula quanto o usuário ganhou ou perdeu.
3. Se o módulo do Cobrador estiver ativo, o bot avisa o resultado puro da aposta no chat _"Você perdeu 100"_. Em seguida, em silêncio, manda os atributos desse resultado para a IA do Cobrador.
4. A IA lê a quantia apostada e tira uma casquinha da desgraça financeira do jogador.
5. O texto do Cobrador é mandado para o chat!

***

## ⚙️ Configurando o Módulo

No Painel de Controle, navegue até **Sistema > IA**. Procure pelo card **"Cobrador Sarcástico (!apostar)"**.

* **Habilitar:** Ative-o para que as vitórias ou perdas nas roletas não passem batidas.
* **Prompt:** Você ditará o grau de crueldade ou humor que esse NPC cobrará a dívida do jogador.

***

## 📝 O Prompt e as Variáveis

Aqui a IA precisa de todas as informações sensíveis sobre a carteira do usuário.

### **Variáveis Disponíveis para o Comando !fala:**

<table><thead><tr><th width="192" align="center"></th><th></th></tr></thead><tbody><tr><td align="center">{username}</td><td>O nome na Twitch de quem abriu o pacote.</td></tr><tr><td align="center">{amount}</td><td>O quanto ele jogou na mesa.</td></tr><tr><td align="center">{result}</td><td>Resultado explícito ("GANHOU" ou "PERDEU").</td></tr><tr><td align="center">{winAmount}</td><td>Se ele tiver ganho, qual o lucro que obteve.</td></tr><tr><td align="center">{totalPoints}</td><td>O quanto de pontos <em>sobrou</em> para ele de saldo na conta geral (o quão perto ele está de pedir esmola).</td></tr><tr><td align="center">{currency}</td><td>O nome da sua moeda personalizada (Gold, Moedas, Pontos).</td></tr></tbody></table>

#### Exemplo de Prompt (Padrão)

> _Você é o "Cobrador Sarcástico", um NPC que adora ver jogadores apostando seus pontos. Um jogador chamado {username} acabou de apostar {amount} pontos e o resultado foi: {result} ({winAmount} ganhos, saldo total: {totalPoints}). Reaja a esse resultado de forma sarcástica, brincalhona ou provocativa (se perdeu) ou com uma ponta de inveja/admiração (se ganhou). Seja breve e use emotes. NÃO usar markdown._

#### Exemplo do Chat

_No chat:_ `FaleComMeuAdvogado apostou 900 Pontos... DERROTA! Saldo atual: 0 Pontos.`

> _"Que belo terno você tinha, {FaleComMeuAdvogado}, é uma pena que agora está no meio da sarjeta de cuecas com zero {Pontos} no bolso. E aí, aceita polir uns troféus em troca de esmola?"_
