# ⁉️ FAQ

## ❓ Perguntas Frequentes (FAQ)

Bem-vindo à nossa central de dúvidas! Aqui você encontra respostas para as perguntas mais comuns divididas por categorias. Clique em uma pergunta para expandir o conteúdo.

***

### 🖥️ Instalação e Configuração

<details>

<summary>1. Como eu consigo o Token Oauth do meu Bot?</summary>

Você deve acessar [TwitchApps TMI](https://twitchapps.com/tmi/) logado na conta que será o BOT e autorizar a aplicação. O código gerado (começando com `oauth:`) deve ser colado nas configurações do servidor.

</details>

<details>

<summary>2. O bot está online mas não responde aos comandos no chat. O que fazer?</summary>

Verifique se o nome do canal nas configurações está exatamente igual ao seu nome de usuário da Twitch. Além disso, certifique-se de que o Token Oauth foi inserido corretamente e que o bot não está banido do seu próprio chat.

</details>

<details>

<summary>3. Como eu adiciono o Baralhada no OBS?</summary>

Crie uma fonte de Navegador (Browser Source), marque a opção "Arquivo Local" e selecione o arquivo `overlay/index.html` dentro da pasta do bot. Recomendamos a resolução 1920x1080.

</details>

***

### ⌨️ Comandos e Interações

<details>

<summary>4. Qual a diferença entre !resgatar e !abrir?</summary>

O comando `!resgatar` é usado para pegar um pacote que apareceu na live (spawn). Já o `!abrir <id_pacote>` é usado para abrir um pacote que já está na sua mochila e transformá-lo em cartas.

</details>

<details>

<summary>5. Meus espectadores reclamam que não ganham pontos. Por quê?</summary>

Os pontos são baseados no tempo de visualização ativa. Certifique-se de que o sistema de pontos está Ativado no painel e que os usuários não estão na lista de bloqueados (`!bloquear`).

</details>

<details>

<summary>6. Como funciona o comando !dica?</summary>

O espectador gasta pontos para receber uma pista de uma carta que ele ainda não tem. O bot esconde parte do nome da carta e tira palavras-chave da descrição para que o chat tente adivinhar.

</details>

***

### 💰 Economia e Itens

<details>

<summary>7. Como eu crio uma carta rara (Lendária)?</summary>

No menu Conteúdo > Cartas, ao criar ou editar uma carta, selecione a Raridade como "Lendária". Lembre-se de configurar uma chance baixa de drop no pacote para manter o valor do item.

</details>

<details>

<summary>8. É possível resetar os pontos de todo mundo para uma nova temporada?</summary>

Sim! No painel de Sistema > Backup, você encontrará a opção de limpeza de banco de dados. Você pode escolher resetar apenas os pontos, mantendo as coleções de cartas se desejar.

</details>

<details>

<summary>9. O que acontece se eu deletar um pacote que as pessoas já têm?</summary>

As pessoas continuarão com as cartas que vieram daquele pacote, mas o pacote em si sumirá da mochila delas. Recomendamos apenas Desativar o pacote em vez de deletar para evitar frustrações.

</details>

***

### 🛡️ Moderação e Segurança

<details>

<summary>10. Como eu impeço um usuário "tóxico" de usar o bot?</summary>

Use o comando `!bloquear @usuario` diretamente no chat ou procure o usuário no menu Comunidade > Usuários e ative a flag de bloqueio.

</details>

<details>

<summary>11. Meus moderadores podem dar cartas para as pessoas?</summary>

Sim, se você der permissão de editor para eles ou se eles usarem o comando `!dar @usuario <id>` no chat (configurável nas permissões de comando).

</details>

***

### 🖼️ Overlays e Visual

<details>

<summary>12. A animação de spawn não está aparecendo no OBS.</summary>

Tente limpar o cache da fonte de navegador no OBS (Propriedades da fonte > Refresh cache of current page). Verifique também se o overlay está Ativado nas configurações do Baralhada.

</details>

<details>

<summary>13. Posso mudar a imagem que aparece no spawn?</summary>

Sim! Cada pacote pode ter sua própria imagem personalizada configurada no menu Conteúdo > Pacotes.

</details>

***

{% hint style="info" %}
Não encontrou sua dúvida? Tente usar o comando `!ajuda` no chat ou verifique os Logs de Sistema para ver se há algum erro sendo reportado.
{% endhint %}
