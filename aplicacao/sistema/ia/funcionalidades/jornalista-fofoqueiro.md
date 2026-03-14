# 📰 Jornalista Fofoqueiro

O **Jornalista Fofoqueiro** é uma atração do chat. Ele resume o que os jogadores andaram aprontando, quem comprou mais, quem perdeu dinheiro e o que está bombando, em tom de tabloide humorístico!

***

## 🛠️ Como Funciona?

O bot rastreia as atividades de todos os usuários desde que o sistema iniciou:

* **Gastos:** Quem perdeu mais Pontos em jogos ou compras.
* **Colecionadores:** Quem abriu mais pacotes ou resgatou mais spawns.
* **Atividade:** Quem mais usou comandos com o bot.

Quando ativado através do comando `!jornal`, a IA assume o papel de um repórter sensacionalista, pegando esses 3 perfis e criando uma manchete e uma matéria recheada de fofoca sobre os jogadores da sua comunidade.

***

## ⚙️ Configurando o Módulo

No Painel de Controle do Baralhada, navegue até **Sistema > IA**. Procure pelo card **"Módulo: Repórter Fofoqueiro"**.

* **Habilitar:** Ligue a chave para que a IA consiga gerar o jornal da fofoca.
* **Prompt (Comando Base):** Defina o estilo do jornal. Pode ser medieval, estilo The Sims, futurista, esporte, etc.

***

## 📝 O Prompt e as Variáveis

Neste modo, a IA interage com as estatísticas gerais da "sessão" ativa. Se você reiniciar o bot, os status (gastões, ativos, etc) da fofoca serão reiniciados para dar espaço aos próximos viewers.

#### Exemplo de Prompt (Padrão)

Este é um exemplo da fofoca padrão do painel:

> Você é um Jornalista Fofoqueiro que adora comentar os eventos do chat. Atue como um locutor de tabloide bem rápido. Resuma o que aconteceu nesta sessão com base nestes dados: Top Gastador: {topSpender}, Top Colecionador: {topCollector}, Usuário mais ativo: {topActive}. Crie uma crônica curtíssima engraçada com humores ácido, engraçado e fofoqueiro. Mencione brigas por cartas e gastos excessivos. NÃO usar markdown.

#### Exemplo do Chat

_No chat:_ `User1 digita !jornal.`

> _"🗞️ **MANCHETE ESPORTIVA DO MEIO-DIA!** 🗞️_
>
> _Alô alô amantes da Baralhada! Nossos repórteres estão de olho vivo. Temos o {BilionárioRusso33} quebrando a banca ali na roleta e esvaziando todas suas economias num pacote comum falido. Vergonhoso. Enquanto isso, cadê os outros inscritos pro spawn? Porque o {NinjaLoot} não dorme e sugou os últimos 4 pacotes que apareceram, uma vergonha o monopólio! Pelo menos ele ainda não tem Lesão de Esforço Repetitivo no dedo como o {FaleComMeuAdvogado} que emitiu mais comandos aqui em 3 horas que as linhas de código do criador deste bot... Aliás, já bebeu ágia hoje criador?!"_

***

## 💡 Informações Importantes

* Se houver um empate, o sistema sorteia um dos maiores valores. Se literalmente ninguém ainda tiver pontuado nada em alguma dessas três métricas nesta sessão, o bot entregará a string `"Ninguém"` para a Inteligência Artificial.
