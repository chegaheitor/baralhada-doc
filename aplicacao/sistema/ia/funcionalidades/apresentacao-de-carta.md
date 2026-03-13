# 🃏 Apresentação de Carta

Este módulo permite que as cartas mais raras e especiais do seu jogo criem uma narrativa personalizada e se apresentem diretamente aos espectadores que as encontram nos pacotes.

_(Quando configurada, a IA reage sempre que o bot detecta o drop de uma carta com a raridade mínima defina por você no painel)._

## 🛠️ Como Funciona?

1. Um espectador usa um comando para abrir um pacote (ex: !abrir).
2. O bot processa o pacote e verifica cada carta revelada.
3. A carta da maior raridade que dropar naquele pacote, faz com que a IA entre em ação.
4. A IA lê as configurações da sua carta, as informações do seu espectador (nome, etc) e a **instrução (prompt) base**.
5. Em alguns segundos, a carta "falará" no chat através do bot.

***

## ⚙️ Configurando o Módulo

No Painel de Controle do Baralhada, navegue até **Sistema > IA > Funcionalidades**. Procure pelo card **"Módulo: Apresentação de Cartas"**.

* **Habilitar:** Ligue a chave para que a IA comunique os drops raros.
* **Prompt (Comando Base):** É aqui que você diz à Inteligência Artificial _como_ ela deve se comportar.

***

## 📝 O Prompt e as Variáveis

O Prompt é o segredo do sucesso. Você tem variáveis especiais (aquelas palavras entre colchetes) que o bot substitui pelas informações reais antes de mandar para a IA.

#### **Variáveis Disponíveis para a Apresentação de Cartas:**

<table><thead><tr><th width="192" align="center"></th><th></th></tr></thead><tbody><tr><td align="center">{username}</td><td>O nome na Twitch de quem abriu o pacote.</td></tr><tr><td align="center">{description}</td><td>A "Lore" (história) base escrita no cadastro da carta.</td></tr><tr><td align="center">{collection}</td><td>A coleção ou pacote a qual ela pertence.</td></tr><tr><td align="center">{rarity}</td><td>A raridade da carta (ex: "Mítica", "Lendária").</td></tr><tr><td align="center">{type}</td><td>O tipo primário da carta (ex: "Criatura", "Feitiço").</td></tr><tr><td align="center">{type2}</td><td>(Opcional) O tipo secundário (ex: "Fogo", "Água").</td></tr><tr><td align="center">{hp}</td><td>A Vida/Defesa base da carta (se aplicável).</td></tr><tr><td align="center">{attack}</td><td>O Poder de Ataque da carta.</td></tr><tr><td align="center">{defense}</td><td>A Armadura ou defesa mágica.</td></tr></tbody></table>

### Exemplo de Prompt (Padrão)

Se você não souber o que colocar, use este modelo:

> _Você é a própria carta {cardName} da coleção {collection}. Apresente-se para {username} enfatizando quem você é, seu propósito e sua história baseada na sua descrição: "{description}". Menções secundárias aos seus atributos (Raridade {rarity}, Tipo {type}/{type2}) e status (HP: {hp}, ATK: {attack}, DEF: {defense}) podem ser feitas para complementar sua identidade. Seja breve, imersivo, use emotes da Twitch e aja como se estivesse honrado em entrar para o deck dele. Máximo de 1000 caracteres. NÃO usar markdown, está proibido!_

### Exemplo do Chat (O que a IA vai gerar e dizer)

No chat: Pipoqueiro\_BR usou !abrir.\
&#xNAN;_(A imagem da carta rara "Dragão do Caos" aparece na live. Após 2 segundos, o Bot digita no chat:)_

> "🔥 Grrr... Finalmente, o selo foi quebrado! Você é o tal do {Pipoqueiro\_BR}? Pensei que quem me invocaria seria alguém maior. Mas tudo bem, meu poder destrutivo de {8000} ATK agora está a seu dispor. Prepare-se, porque a Coleção {Chamas Antigas} acaba de ficar pequena para nós dois. Sou o Dragão do Caos, vamos incendiar isso tudo!"

***

## 💡 Dicas de Uso

* **Não use descrições genéricas no cadastro da carta:** A IA fica mais criativa quanto melhor e mais bem escrita for a {description} da sua carta no painel. Pense em quem escreveu aquilo e coloque a lore!
* **Tempo de Resposta:** Vale lembrar que a IA pode demorar de 2 a 15 segundos para formular o texto.&#x20;
