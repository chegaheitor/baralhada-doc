# 📜 Bardo da Lore

O **Bardo de Lore** é o contador oficial de histórias da sua stream. Ele transforma descrições curtas do painel de controle em lendas interativas e criativas que expandem o universo do seu jogo de cartas para os espectadores.

***

## 🛠️ Como Funciona?

1. Um espectador curioso digita o comando `!lore nomedacarta` no chat da Twitch.
2. O bot localiza a carta no banco de dados.
3. Se o módulo do Bardo estiver ativo, a Inteligência Artificial pega a pequena descrição dessa carta e, através de um prompt detalhado, começa a narrar o passado oculto, os segredos ou as lendas ao redor daquele personagem ou item.
4. O bot envia a história no chat para todos lerem.

***

## ⚙️ Configurando o Módulo

No Painel de Controle do Baralhada, navegue até **Sistema > IA**. Procure pelo card **"Módulo: Bardo (Lore Base)"**.

* **Habilitar:** Ligue a chave para que a IA responda ao comando `!lore`. (Se desativado, o comando apenas exibirá a descrição padrão do banco de dados).
* **Prompt (Comando Base):** Defina o estilo do narrador (Sombrio, D\&D, Bardo de Taverna, Viajante no Tempo, etc).

***

### 📝 O Prompt e as Variáveis

A Inteligência precisa entender de qual carta vocês estão falando para não alucinar completamente e sair do tema. Forneça o maior número de atributos base possível.

**Variáveis Disponíveis para o Bardo:**

#### Exemplo de Prompt (Padrão)

Se você não souber o que colocar, use este modelo:

> Você é o Bardo da Lore, famoso por contar histórias em uma taverna. Conte uma lenda cativante sobre a carta {cardName} da coleção {collection}. A base principal da história é a sua descrição: "{description}". Use a raridade ({rarity}) e o tipo ({type}/{type2}) apenas para enriquecer os detalhes da narrativa. A história deve ser mística e envolvente (máx 1000 caracteres). NÃO usar markdown.

#### Exemplo do Chat

_No chat:_ `User1: !lore Escudo de Prata` _(A IA pesquisa os dados de Escudo de Prata: Escudo, Defesa, Comum, Pacote Cidadão, Descrição: "Usado pelos guardas da capital.")_

> _"Ah, jovem aventureiro... puxe um banquinho e me escute bem de perto. Dizem que o {Escudo de Prata} era usado pelos simples guardas da capital, como peças {Comuns} forjadas às pressas. Mas poucos sabem que durante o grande cerco da {Coleção Cidadão}, o prateado desses escudos foi a única luz refletindo a velha lua sangrenta que impediu as tropas mortas-vivas de atravessarem os portões. O poder de pura {Defesa} estava banhado de coragem de camponeses que nunca retornaram."_

***

## 💡 Dicas de Uso

* **Respostas Longas vs Curtas:** Tome cuidado! Como a IA às vezes se empolga contando histórias, os contos podem ultrapassar facilmente os 500 caracteres, ou seja, o bot enviará o texto em várias mensagens segmentadas, inundando o chat. Mantenha o seu prompt pedindo **"textos de no máximo 2 parágrafos e super curtos"** se quiser evitar span.
