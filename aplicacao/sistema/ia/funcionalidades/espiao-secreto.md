# 🕵️ Espião Secreto

O **Espião Secreto** é o contato misterioso que ajuda os novos colecionadores a localizarem as cartas que faltam para completarem seus álbuns. Usando o comando `!dica`, os jogadores pagam um valor subornado para a IA soltar fofocas de qual baú, pessoa ou lugar a carta perdida pode estar escondida.

***

## 🛠️ Como Funciona?

1. Um usuário não consegue completar uma coleção. Ele usa `!dica Nome_Colecao` pagando pontos do sistema.
2. O bot vasculha o banco de dados daquela coleção em específico e encontra qual a carta mais fraca/comum que o jogador não possui no deck dele.
3. Se o Espião Secreto estiver ativo, o bot envia os dados dessa carta _exata_ para a IA.
4. A IA gera um enigma: não entregando o nome diretamente, mas fazendo charadas com as palavras da Lore, as Letras ocultas ou tipo de ataque para o usuário tentar tentar pescar a ideia sobre como abrir essa coleção.
5. O texto do Enigma é impresso no chat!

***

## ⚙️ Configurando o Módulo

No Painel de Controle, navegue até **Sistema > IA**. Procure pelo card **"Espião Secreto (!dica)"**.

* **Habilitar:** Ative-o para que a IA gere as charadas. Se o mesmo não estiver habilitado, o bot ainda dirá qual carta falta e onde encontrá-la, mas de modo direto e chatinho.
* **Prompt (Comando Base):** Você ditá aqui a "Vibe" desse informante. Ele está num beco escuro? Numa taverna?

***

### 📝 O Prompt e as Variáveis

Aqui a IA precisa de informações preciosas sobre a _"carta que falta"_, e então, não se esqueça de proibir a IA de contar o nome absoluto da carta, afinal é uma DICA!

#### Exemplo de Prompt (Padrão e Exato)

Para este caso, a IA precisa de um toque charlatão, para ela disfarçar a descrição:

> _Você é um espião secreto infiltrado no submundo das cartas que vende informações secretas. Dê uma dica enigmática e instigante sobre a carta {cardName} da coleção {collection}. O foco da dica deve ser o que a carta representa e sua lore contida na descrição: "{description}". Detalhes como tipo ({type}/{type2}) e raridade ({rarity}) devem vir em segundo plano. Não diga o nome limpo da carta em hipótese alguma! O ID parcial é {maskedId}. Seja breve e misterioso. NÃO usar markdown._

#### Exemplo do Chat

_No chat:_ `FaleComMeuAdvogado compra dica para a coleção Inverno Sombrio.` _(Falta a carta Rei Gelado para completar a Coleção)_

> _"(Sussurro) Pssst! Chegue mais perto, {FaleComMeuAdvogado}. Diz a lenda que dentro dos portões de aço da {caixa Cidadão} descansam as almas que não encontram a paz. Procure pelo {Senhor Gélido Coroado}... Você tem 5 moedas de ouro para fingir que não tivemos essa conversa, saia."_
