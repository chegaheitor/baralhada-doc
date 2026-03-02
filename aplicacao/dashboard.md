# Dashboard

## 📊 Dashboard

O Painel Administrativo é o centro de comando do seu bot. Na aba inicial (Dashboard), você tem uma visão panorâmica de tudo o que está acontecendo.



#### 🤖 Status do Bot

Indicador visual em tempo real — 🟢 verde (online) ou 🔴 vermelho (offline). Botão de ligar/desligar também fica aqui no dashboard.

#### ℹ Cards Rápidos

Cards com informações rápidas do bot e sua comunidade.

<table data-view="cards"><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Usuários</td><td>Quantidade de usuários cadastrados no Baralhada.</td></tr><tr><td>Cartas em circulação</td><td>Nº de cartas que todos os usuários possuem.</td></tr><tr><td>Total de pontos</td><td>Soma de todos os pontos que os usuários possuem.</td></tr><tr><td>Próximo spawn</td><td>Timer que mostra quando será o próximo spawn programado.</td></tr></tbody></table>

#### 🟦 Navegação Rápida

Links diretos para as seções mais usadas: Spawns, Usuários, Loja, Missões, Estatísticas.

#### 📊 Rankings

**Top Colecionadores** — usuários com mais cartas de toda a plataforma.

#### 📋 Feed de Logs ao Vivo

As últimas ações registradas pelo sistema em tempo real, com tipos: `SUCCESS`, `INFO`, `WARN`, `ERROR`.

{% hint style="info" %}
Deixe o painel aberto em um segundo monitor para monitorar a atividade e reagir rapidamente a eventos de spawn!
{% endhint %}

***

## Cartas

### O que é uma Carta

Cartas são os itens colecionáveis fundamentais do jogo. Cada carta tem:

| Campo               | Descrição                             |
| ------------------- | ------------------------------------- |
| **Nome**            | Nome exibido no chat e painel         |
| **Slug**            | Identificador único (sem espaços)     |
| **Número**          | Número na coleção                     |
| **Coleção**         | Coleção à qual pertence               |
| **Raridade**        | Comum, Incomum, Rara, Épica, Lendária |
| **Tipo**            | Tipo primário da carta                |
| **Tipo 2**          | Tipo secundário (opcional)            |
| **HP**              | Pontos de vida (cosmético)            |
| **Imagem**          | URL ou upload local                   |
| **Preço de Compra** | Pontos para comprar na loja           |
| **Preço de Venda**  | Pontos recebidos ao vender            |
| **Comprável**       | Se aparece na loja                    |
| **Vendável**        | Se pode ser vendida                   |
| **Ativa**           | Se está disponível no jogo            |

### Gerenciando Cartas

No Painel Admin → Cartas:

* Crie, edite e exclua cartas
* Filtre por coleção ou raridade
* Faça upload de imagem diretamente pelo painel
* Organize por número dentro de cada coleção

***

## Pacotes

### O que é um Pacote

Pacotes são envelopes que contêm cartas aleatórias. Podem ser obtidos via spawn, compra na loja ou via presente.

| Campo                     | Descrição                                         |
| ------------------------- | ------------------------------------------------- |
| **Nome / Slug**           | Identificação                                     |
| **Imagem**                | Arte do pacote                                    |
| **Cartas por Pack**       | Quantas cartas saem ao abrir                      |
| **Chances de Raridade**   | Probabilidade de cada raridade (%)                |
| **Cartas Permitidas**     | Filtrar de quais cartas pode sair (vazio = todas) |
| **Tipo de Claim**         | `fastest` ou `raffle`                             |
| **% do Raffle**           | Porcentagem que ganha no modo sorteio             |
| **Duração do Spawn**      | Segundos que o spawn fica ativo                   |
| **Pontos ao Abrir**       | XP/pontos dados ao abrir                          |
| **Preço de Compra/Venda** | Para loja                                         |
| **Comprável / Vendável**  | Se aparece na loja                                |
| **Mensagem de Spawn**     | Texto personalizado quando spawna                 |

***

## Spawns / Eventos

Spawns são os eventos automáticos que lançam itens no chat.

### Criando um Spawn

{% stepper %}
{% step %}
### Acessar Spawns

Vá em **Painel → Spawns**.
{% endstep %}

{% step %}
### Novo Evento

Clique em **Novo Evento**.
{% endstep %}

{% step %}
### Selecionar Pacote

Selecione o **Pacote** que será lançado.
{% endstep %}

{% step %}
### Configurar Intervalo

Configure o **Intervalo** (em minutos) entre spawns.
{% endstep %}

{% step %}
### Ativar Spawn

Ative o spawn.
{% endstep %}
{% endstepper %}

### Múltiplos Spawners

Você pode ter vários spawners ativos simultaneamente, cada um com seu próprio timer e pacote. Isso permite criar eventos diferentes rodando em paralelo.

### Mensagem de Spawn Personalizada

Cada pacote pode ter uma mensagem de spawn customizada. Variáveis disponíveis:

```
{pack_name} — nome do pacote
{claim_type} — tipo de claim
```
