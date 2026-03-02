# Usuarios

## Visão Geral

A página de Usuários mostra todos os viewers que já interagiram com o bot. Os dados são sincronizados com o Twitch (foto de perfil, username).

## Lista de Usuários

Cada linha mostra:

* **Foto e Username** do Twitch
* **Pontos** atuais
* **Nível** (baseado em XP acumulado)
* **Status:** Ativo ou Bloqueado
* **Ações:** Editar pontos, ver inventário, bloquear

## Editar Pontos

{% stepper %}
{% step %}
### Editar pontos

* Clique no ícone de edição (🖊️) ao lado do usuário
{% endstep %}

{% step %}
### Digitar novo valor

* Digite o novo valor de pontos
{% endstep %}

{% step %}
### Salvar

* Clique em Salvar
{% endstep %}
{% endstepper %}

## Bloquear / Desbloquear

{% stepper %}
{% step %}
### Bloquear usuário

* Clique no ícone de escudo ao lado do usuário
{% endstep %}

{% step %}
### Confirmar

* Confirme a ação
{% endstep %}

{% step %}
### Desbloquear

* Para desbloquear, clique novamente no mesmo ícone
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
Usuários bloqueados não podem usar nenhum comando do bot.
{% endhint %}

## Gerenciar Inventário

Clique no ícone de inventário (🎒) para abrir o painel de inventário do usuário.

### Ver Cartas

Lista todas as cartas com imagem, nome e raridade com código de cor.

### Ver Pacotes

Lista todos os pacotes com imagem, nome e quantidade.

### Adicionar Item

{% stepper %}
{% step %}
### Iniciar adição

* Clique em **+ Adicionar Item**
{% endstep %}

{% step %}
### Escolher tipo

* Escolha entre **Carta** ou **Pacote**
{% endstep %}

{% step %}
### Pesquisar

* Pesquise o item pelo nome
{% endstep %}

{% step %}
### Selecionar

* Selecione o item na galeria visual
{% endstep %}

{% step %}
### Quantidade

* Defina a quantidade
{% endstep %}

{% step %}
### Confirmar

* Confirme
{% endstep %}
{% endstepper %}

### Remover Item

* Clique no ícone de lixeira ao lado de qualquer item para removê-lo do inventário.

## Pesquisa

Use a barra de pesquisa no topo da lista de usuários para filtrar por username.
