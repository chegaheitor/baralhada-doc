# ✨ Spawns/Eventos

## 🕹️ O que é um Spawn

Um spawn é um evento automático onde um pacote "aparece" no chat da live e os espectadores podem pegar com `!resgatar`. O streamer configura quais eventos acontecem, com qual frequência e qual pacote é lançado.

#### Como Funciona

O bot monitora timers configurados no Painel Admin. Quando o tempo de um spawn atinge o intervalo definido, o bot seleciona aleatoriamente um dos pacotes vinculados àquele spawn e o lança no chat com um alerta visual no overlay.

## Criando um Spawn

{% stepper %}
{% step %}
### Vá em **Painel → Spawns**.

Aqui você define todos os eventos de spawn!
{% endstep %}

{% step %}
### Novo Evento

Clique em **Novo Evento**.
{% endstep %}

{% step %}
### Configure

Preencha os campos:

| Campo               | Descrição                                                        |
| ------------------- | ---------------------------------------------------------------- |
| **Nome do Evento**  | Determina o nome do evento                                       |
| **Intervalo (min)** | De quantos em quantos minutos o spawn ocorre                     |
| **Pacotes**         | Qual pacote será lançado neste spawner                           |
| **Cofre da Sorte**  | Porcentagem do comando !cofre\_sorte spawnar como evento no chat |
| **Ativo**           | Ligar/desligar este spawner                                      |
{% endstep %}
{% endstepper %}

## 🌐 Múltiplos Spawners

Você pode criar vários spawners simultâneos, cada um com seu próprio timer e pacote. Isso permite:

* Um spawn de Pacote Básico a cada 10 minutos
* Um spawn de Pacote Raro a cada 45 minutos
* Um spawn de Pacote Lendário uma vez por hora

Todos rodam de forma independente.

## Comportamento do Spawn

{% stepper %}
{% step %}
### Anúncio

O bot anuncia no chat com a mensagem configurada no pacote (`spawn_message`).
{% endstep %}

{% step %}
### Duração para claim

O timer de `custom_duration` começa (segundos disponíveis para `!claim`).
{% endstep %}

{% step %}
### Reivindicação

Usuários usam `!claim`.
{% endstep %}

{% step %}
### Entrega do item

Dependendo do tipo (`fastest` ou `raffle`), o item é entregue.
{% endstep %}

{% step %}
### Encerramento

O spawn encerra e o timer do próximo começa.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Dica: Configure spawns mais frequentes nos horários de pico da sua live para maximizar o engajamento. Use intervalos mais longos em horários de baixo público para criar raridade.
{% endhint %}

## Mensagem Personalizada

Cada pacote possui um campo `spawn_message` para personalizar o texto que aparece no chat quando ele spawna. Exemplo:

```
📦 Um Pacote Lendário apareceu! Use !claim para tentar pegar! Duração: 60 segundos 🎴
```

{% hint style="info" %}
Use o **Spawn Manual** no Dashboard para disparar um evento emocionante em momentos de pico da live ou como recompensa por uma meta batida!
{% endhint %}

## 🚀 Spawn Manual

Precisa de um drop instantâneo? No Dashboard, clique em **Spawn Manual**, selecione o pacote e ele cairá na hora no chat, independente de qualquer configuração de timer.

{% hint style="warning" %}
Verifique se os pacotes selecionados possuem cartas configuradas dentro deles, caso contrário o espectador ganhará um pacote vazio.
{% endhint %}

## 🍀 Cofre da Sorte

A funcionalidade [Cofre da Sorte](../../comandos/administracao/cofre-da-sorte.md) pode ser utilizada como se fosse um spawn. Configure as chances dele ser spawnado e ao invés de ser spawnado um pacote, o Baralhada spawna um Cofre da Sorte para os viewers, automatizando o comando.

