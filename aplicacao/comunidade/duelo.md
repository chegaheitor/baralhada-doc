# ⚔️ Duelo

## 🏟️ O que é o Sistema de Duelos

O sistema de duelos permite que os viewers testem o poder de suas coleções em combates diretos no chat. É uma forma estratégica de ganhar pontos (aposta) ou simplesmente demonstrar a superioridade de suas cartas através de atributos e tipagens.

### 🕹️ Como Iniciar um Duelo

Siga os passos abaixo para desafiar um oponente no chat:

{% stepper %}
{% step %}
### ⚔️ O Desafio

Escolha um oponente e a carta que você deseja usar.

* **Comando**: `!duelo @usuario <slug_da_carta> <aposta>`
* **Exemplo**: `!duelo @Bob dragao_azul 500`
{% endstep %}

{% step %}
### 🛡️ A Defesa

O oponente deve responder ao desafio com sua própria carta.

* **Comando**: `!defesa <slug_da_minha_carta>`
* **Exemplo**: `!defesa fenix_fogo`
{% endstep %}

{% step %}
### 🏆 O Resultado

O bot calcula o vencedor baseado nos atributos, pesos e vantagens de tipo. Os pontos são transferidos instantaneamente.
{% endstep %}
{% endstepper %}

## ⚖️ Configuração de Pesos

No painel administrativo (**Configurações de Duelo**), você ajusta o equilíbrio do combate definindo a importância de cada atributo:

<table><thead><tr><th width="150">Atributo</th><th width="100">Tipo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Peso de HP</strong></td><td>Decimal</td><td>Multiplicador dos pontos de vida. Aumenta a duração da luta.</td></tr><tr><td><strong>Peso de ATK</strong></td><td>Decimal</td><td>Multiplicador do dano bruto causado por turno.</td></tr><tr><td><strong>Peso de DEF</strong></td><td>Decimal</td><td>Reduz o dano recebido.</td></tr></tbody></table>

{% hint style="info" %}
O sistema calcula o dano por turno: \`Dano = (ATK \* Bônus\_Tipo) - (DEF\_Oponente / 2)\`. Vence quem reduzir o HP do oponente a zero primeiro.
{% endhint %}

## 💥 Sistema de Tipagem (Estratégia)

As vantagens de tipo são o segredo para vencer oponentes mais fortes. Cada tipo tem um multiplicador de bônus ou penalidade.

* **Vantagem Primária**: Bônus de ataque se o Tipo 1 for forte contra o oponente.
* **Vantagem Secundária**: Bônus adicional se o Tipo 2 também for favorável.
* **Penalidade**: Redução de ataque se o seu tipo for fraco contra o oponente.

{% hint style="success" %}
**Exemplo de Bônus**: Se sua carta tem vantagem de **30%**, um ataque de **100** sobe para **130**! Isso pode ignorar defesas altas.
{% endhint %}

## &#x20;📝 Exemplo de Turno Real

Veja como uma rodada é processada pelo bot:

{% stepper %}
{% step %}
Alice (🔥 Fogo) vs Bob (❄️ Gelo)&#x20;

Alice ataca com **Dragão (100 ATK)**. Como Fogo vence Gelo, Alice ganha **+30% de bônus**.

* **ATK Final Alice**: 130
{% endstep %}

{% step %}
Cálculo de Dano Bob tem **40 de DEF**. O dano de Alice será:

* `130 - (40 / 2) = 110 de Dano Útil`
{% endstep %}

{% step %}
Vitória! Se Bob tem **200 de HP**, ele será derrotado em apenas **2 turnos** por Alice.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
**Atenção**: Se o oponente não tiver pontos suficientes para cobrir a aposta no momento da aceitação, o duelo será cancelado automaticamente pelo bot.
{% endhint %}
