# Como funciona

## O Ciclo de Jogo

```
Live começa
    ↓
Bot conecta ao chat do canal
    ↓
Spawns aparecem automaticamente no chat
    ↓
Espectadores usam !resgatar para pegar o spawn
    ↓
Cartas vão para o inventário do usuário
    ↓
Usuários abrem pacotes (!abrir), compram (!comprar), vendem (!vender) e trocam (!troca)
    ↓
Ganham pontos ao assistir a live e realizar ações
    ↓
Completam missões e álbuns para ganhar recompensas
```

***

## Pontos

Os **pontos** são a moeda do jogo. Os usuários acumulam pontos:

* Ficando na live (por tempo assistido, configurável)
* Vendendo cartas e pacotes na loja
* Pela recompensa diária (`!daily`)

Os pontos são usados para **comprar itens na loja** (`!comprar`).

***

## XP e Nível

Além dos pontos, os usuários ganham **XP** e sobem de **nível** ao interagir:

* Claim de spawns
* Abertura de pacotes
* Missões completadas

O nível não tem efeito mecânico, mas serve como indicador de engajamento e pode ser exibido no ranking.

***

## Spawns

**Spawns** são eventos onde uma carta ou pacote aparece no chat e qualquer pessoa pode pegar. Existem dois tipos de claim:

| Tipo               | Descrição                                                                          |
| ------------------ | ---------------------------------------------------------------------------------- |
| `Rápido (fastest)` | O primeiro a usar `!resgatar` fica com o item                                      |
| `Sorteio (raffle)` | Todos que usam `!resgatar` entram no sorteio, e uma porcentagem configurável ganha |

O streamer pode criar múltiplos spawns com timers independentes, cada um associado a um ou mais pacote específico.

***

## Fluxo de Trade

{% stepper %}
{% step %}
### Iniciar troca

Usuário A digita `!troca @UsuarioB [carta]`
{% endstep %}

{% step %}
### Pedido enviado

Um pedido de troca é enviado para o Usuário B
{% endstep %}

{% step %}
### Aceitar ou recusar

O Usuário B tem um tempo para aceitar com `!tradeOffer aceitar` ou recusar com `!tradeOffer recusar`
{% endstep %}

{% step %}
### Troca concluída

Se aceito, os itens são trocados automaticamente
{% endstep %}
{% endstepper %}

***

## Banco de Dados

O Baralhada Bot usa **NeDB** — um banco de dados embutido que armazena tudo em arquivos locais na pasta de dados do seu sistema (`AppData/Roaming/baralhada-bot` no Windows). Nenhum dado é enviado para servidores externos.
