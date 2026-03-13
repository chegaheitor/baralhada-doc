# 🗣️ Comando !fala

O módulo **Comando !fala** permite que os espectadores conversem diretamente com as cartas do seu deck ativo. A IA assume a personalidade da carta solicitada e responde às asneiras, perguntas ou cantadas dos seus viewers em tempo real.

## 🛠️ Como Funciona?

1. O bot localiza a carta ativa no "deck" do usuário que disparou o comando.
2. O usuário manda uma mensagem no chat usando o atalho `!fala nomedacarta mensagem` (Ex: `!fala Dragão qual o seu prato favorito?`).
3. O bot intercepta a mensagem, olha os atributos dessa carta (lore, vida, ataque) e envia junto com a pergunta para a Inteligência Artificial.
4. A IA gera uma resposta baseada na personalidade da carta e na mensagem do espectador.
5. O bot fala a resposta no chat.

{% hint style="info" %}
O comando !fala exige que o usuário possua a carta. Se não possuir, o bot retornará erro.
{% endhint %}

## ⚙️ Configurando o Módulo

No Painel de Controle, navegue até **Sistema > IA**. Procure pelo card **"Módulo: Conversa Direta (!fala)"**.

* **Habilitar:** Ative para permitir que as cartas ganhem vida com o comando.
* **Prompt (Comando Base):** É aqui que você dá a diretriz principal de como todas as cartas devem reagir aos humanos.

## 📝 O Prompt e as Variáveis

Aqui a IA precisa de todas as informações sobre a sua carta para conseguir incorporá-ela satisfatoriamente na conversa.

### **Variáveis Disponíveis para o Comando !fala:**

<table><thead><tr><th width="192" align="center"></th><th></th></tr></thead><tbody><tr><td align="center">{username}</td><td>O nome na Twitch de quem abriu o pacote.</td></tr><tr><td align="center">{message}</td><td>A pergunta ou frase enviada pelo espectador.</td></tr><tr><td align="center">{description}</td><td>A "Lore" (história) base escrita no cadastro da carta.</td></tr><tr><td align="center">{collection}</td><td>A coleção ou pacote a qual ela pertence.</td></tr><tr><td align="center">{rarity}</td><td>A raridade da carta (ex: "Mítica", "Lendária").</td></tr><tr><td align="center">{type}</td><td>O tipo primário da carta (ex: "Criatura", "Feitiço").</td></tr><tr><td align="center">{type2}</td><td>(Opcional) O tipo secundário (ex: "Fogo", "Água").</td></tr><tr><td align="center">{hp}</td><td>A Vida/Defesa base da carta (se aplicável).</td></tr><tr><td align="center">{attack}</td><td>O Poder de Ataque da carta.</td></tr><tr><td align="center">{defense}</td><td>A Armadura ou defesa mágica.</td></tr></tbody></table>

### Exemplo de Prompt (Padrão)

> _Você é a própria carta {cardName} da coleção {collection}. Responda à mensagem do viewer {viewer} incorporando sua essência, história e propósito descritos aqui: "{description}". Use seus atributos técnicos (Raridade {rarity}, Tipo {type}/{type2}, Status HP {hp}/ATK {attack}/DEF {defense}) apenas como suporte para sua personalidade. Mensagem: "{message}". Seja breve, no personagem e NÃO use markdown._

#### Exemplo do Chat

_No chat:_ `Pipoqueiro_BR: !fala Dragão você gosta de marshmallow avermelhado?`

> _"Eu sou um Dragão do Caos de 8000 de Ataque, {Pipoqueiro\_BR}, as chamas do abismo correm nas minhas veias. Acha mesmo que eu me importo com seus doces humanos macios? (Mas se você tiver um pedaço de cavaleiro torrado, eu aceito)."_

## 💡 Dicas de Uso

* Manter a regra de "2 linhas" no prompt ajuda a evitar que a IA gaste os 1500 caracteres estipulados de conversinhas banais no chat, tornando as interações dinâmicas e engraçadas.
