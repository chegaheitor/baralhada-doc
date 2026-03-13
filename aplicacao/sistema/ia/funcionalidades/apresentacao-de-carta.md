# Apresentação de Carta

Este módulo permite que as cartas mais raras e especiais do seu jogo criem uma narrativa personalizada e se apresentem diretamente aos espectadores que as encontram nos pacotes.

_(Quando configurada, a IA reage sempre que o bot detecta o drop de uma carta com a raridade mínima defina por você no painel)._

## 🛠️ Como Funciona?

1. Um espectador usa um comando para abrir um pacote (ex: !abrir).
2. O bot processa o pacote e verifica cada carta revelada.
3. Se a raridade da(s) carta(s) for maior ou igual ao limite configurado (ex: Ouro, Lendária, etc.), a IA entra em ação.
4. A IA lê as configurações da sua carta, as informações do seu espectador (nome, etc) e a **instrução (prompt) base**.
5. Em alguns segundos, a carta "falará" no chat através do bot.

***

## ⚙️ Configurando o Módulo

No Painel de Controle do Baralhada, navegue até **Sistema > IA**. Procure pelo card **"Módulo: Apresentação Rara (Drops)"**.

* **Habilitar:** Ligue a chave para que a IA comunique os drops raros.
* **Raridade Mínima (Threshold):** Defina a partir de qual raridade a IA começará a narrar. _Dica: Configure apenas para cartas muito raras (ex: Lendárias, Míticas) para evitar spam no chat em pacotes comuns._
* **Prompt (Comando Base):** É aqui que você diz à Inteligência Artificial _como_ ela deve se comportar.

***

## 📝 O Prompt e as Variáveis

O Prompt é o segredo do sucesso. Você tem variáveis especiais (aquelas palavras entre colchetes) que o bot substitui pelas informações reais antes de mandar para a IA.

**Variáveis Disponíveis para a Apresentação de Cartas:**

* {username}: O nome na Twitch de quem abriu o pacote.
* {rarity}: A raridade da carta (ex: "Mítica", "Lendária").
* {type}: O tipo primário da carta (ex: "Criatura", "Feitiço").
* {type2}: (Opcional) O tipo secundário (ex: "Fogo", "Água").
* {collection}: A coleção ou pacote a qual ela pertence.
* {hp}: A Vida/Defesa base da carta (se aplicável).
* {attack}: O Poder de Ataque da carta.
* {defense}: A Armadura ou defesa mágica.
* {description}: A "Lore" (história) base escrita no cadastro da carta.

### Exemplo de Prompt (Padrão)

Se você não souber o que colocar, use este modelo:

> _"Atue como um narrador épico! O jogador {username} acaba de tirar de um pacote a incrível e raríssima ({rarity}) carta. O nome da carta tirada é a primeira coisa que você deve descobrir se apresentando. Ela é do tipo {type} {type2} e pertence à coleção {collection}. Seus atributos são ATK: {attack}, DEF: {defense}. Histórico dela: {description}. Faça com que essa carta converse diretamente com {username}, impressionada por ter sido invocada por ele, com um tom misterioso mas amigável. Diga algo único sobre seus atributos."_

### Exemplo do Chat (O que a IA vai gerar e dizer)

_No chat:_ \Pipoqueiro\_BR usou !abrir.\
&#xNAN;_(A imagem da carta rara "Dragão do Caos" aparece na live. Após 2 segundos, o Bot digita no chat:)_

> "🔥 Grrr... Finalmente, o selo foi quebrado! Você é o tal do {Pipoqueiro\_BR}? Pensei que quem me invocaria seria alguém maior. Mas tudo bem, meu poder destrutivo de {8000} ATK agora está a seu dispor. Prepare-se, porque a Coleção {Chamas Antigas} acaba de ficar pequena para nós dois. Sou o Dragão do Caos, vamos incendiar isso tudo!"

***

## 💡 Dicas de Uso

* **Não use descrições genéricas no cadastro da carta:** A IA fica mais criativa quanto melhor e mais bem escrita for a {description} da sua carta no painel. Pense em quem escreveu aquilo e coloque a lore!
* **Tempo de Resposta:** Vale lembrar que a IA pode demorar de 2 a 15 segundos para formular o texto. Recomendamos o uso de áudios curtos ou animações mais longas na sua OBS para disfarçar o tempo de processamento.
