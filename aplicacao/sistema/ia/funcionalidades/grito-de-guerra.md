# ⚔️ Grito de Guerra

O **Grito de Guerra** eleva a emoção dos duelos no chat. Em vez de apenas mostrar quem ganhou ou perdeu baseando-se em números frios, a IA assume o papel de um locutor de arena e dos próprios combatentes, narrando as provocações antes do embate.

***

## 🛠️ Como Funciona?

1. Um jogador desafia o outro usando `!atacar @alvo slug_da_carta (aposta)`.
2. O alvo aceita o desafio usando `!defesa slug_da_carta`.
3. O bot intercepta o duelo antes dos cálculos matemáticos.
4. A IA lê a lore e os status das duas cartas envolvidas.
5. A IA gera um texto em 3 partes separadas por um pipe (`|`):
   * A provocação da carta atacante.
   * A resposta desafiadora da carta defensora.
   * A narração épica do locutor antes do confronto começar.
6. O bot envia essas três mensagens sequencialmente no chat antes de revelar o grande vencedor.

***

## ⚙️ Configurando o Módulo

No Painel de Controle do Baralhada, navegue até **Sistema > IA**. Procure pelo card **"Módulo: Grito de Guerra (Duelos)"**.

* **Habilitar:** Ligue a chave para ativar as narrações de duelo.
* **Prompt (Comando Base):** É aqui que você diz à Inteligência Artificial as regras de formatação do texto. _Cuidado ao alterar para não quebrar o formato com pipes `|`_.

***

### 📝 O Prompt e as Variáveis

O sistema precisa de instruções estritas para garantir que o bot consiga dividir o texto nas 3 falas (Atacante, Defensor, Locutor).

#### Exemplo de Prompt (Padrão e Recomendado)

Este prompt é meticulosamente montado para obrigar a IA a formatar a resposta usando o delimitador `|`.

> Você é um narrador de duelos épicos e as próprias cartas de combate. Gere um confronto verbal de provocação curto entre {attackerName} e {defenderName}. A provocação de {attackerName} deve ser baseada em sua história e propósito ({attackerDescription}), e a resposta de {defenderName} deve refletir sua própria história e propósito ({defenderDescription}). Como narrador, anuncie com empolgação o início do duelo. Formato: {attackerName}: \[provocação] | {defenderName}: \[resposta] | Narrador: \[anúncio]. NÃO usar markdown.

#### Exemplo do Chat (A narração)

_No chat:_ `Pipoqueiro_BR aceitou o duelo com Espadachim de Prata!`

> **Espadachim de Prata:** "Vou fatiar suas escamas e fazer uma bota com elas, largatixa crescida!" **Dragão do Caos:** "Você vai derreter na sua própria armadura de latão antes mesmo de encostar em mim." **Locutor:** "O clima esquentou na arena! O aço prateado contra as chamas caóticas! QUEM SAIRÁ VIVO DESSE EMBATE?!"

_(Segundos depois, o bot envia o resultado oficial do duelo calculando os atributos)._

***

### 💡 Informações Importantes

* **Pipes são obrigatórios:** A inteligência precisará sempre retornar o texto dividido em 3 pedaços usando o caractere `|`. O bot usa isso para "fatiar" a resposta e mandar 3 mensagens no chat simulando uma conversa.
* **Tratamento de Erros:** Caso a IA tenha algum erro ou timeout (demore mais de 30s) para gerar a história, o bot ignora o erro e prossegue imediatamente para o cálculo do resultado do duelo, garantindo que o jogo não pare.
