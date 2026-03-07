# 🏪 Marketplace

## 💰 O que é o Marketplace

O bot possui um sistema econômico robusto que permite que os viewers comprem e vendam itens. Existem duas formas de comércio: a **Loja Rotativa** (NPC) e o **Marketplace** (P2P).

## 👥 Marketplace (Jogador para Jogador)

O Marketplace é onde os viewers anunciam suas próprias cartas e pacotes para que outros comprem.

{% stepper %}
{% step %}
### 📝 Anunciar

Escolha um item do seu inventário e defina um preço.

* **Comando**: `!anunciar <slug_do_item> <preço>`
* **Exemplo**: `!anunciar dragao_azul 2000`
{% endstep %}

{% step %}
### 🔍 Ver Itens

Consulte o que está à venda no momento.

* **Comando**: `!marketplace`
* **Resposta**: O bot envia a lista completa via Sussurro.
{% endstep %}

{% step %}
### 💰 Comprar

Interessado em um item? Use o ID fornecido na lista.

* **Comando**: `!comprar_market <id_do_anuncio>`
* **Exemplo**: `!comprar_market 123`
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
**Regra do Market**: Quando você anuncia um item, ele sai do seu inventário e "mora" no marketplace até ser comprado ou o anúncio ser cancelado (via Painel Admin).
{% endhint %}

***

## 🎭 Loja Rotativa

A Loja do Reino é uma loja automática que rotaciona itens com **descontos exclusivos**.

#### 📝 Comandos da Loja:

<table><thead><tr><th width="216">Comando</th><th>Ação</th></tr></thead><tbody><tr><td><code>!loja</code></td><td>Exibe o inventário do Reino e cronômetro de rotação (Sussurro).</td></tr><tr><td><code>!loja_comprar &#x3C;id></code></td><td>Compra o item promocional selecionado.</td></tr></tbody></table>

{% hint style="success" %}
Os itens na Loja do Reino sempre vêm com desconto (ex: 10% a 30% mais barato que o preço base).
{% endhint %}

## ⚙️ Configurações da Rodada

No **Painel Admin → Marketplace**, você configura o comportamento automático do Reino:

<table><thead><tr><th width="150">Campo</th><th width="100">Valor</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Itens na Loja</strong></td><td>Número</td><td>Quantos itens serão sorteados por vez.</td></tr><tr><td><strong>Janela de Rotação</strong></td><td>Horas</td><td>De quanto em quanto tempo a loja renova o estoque.</td></tr><tr><td><strong>Descontos</strong></td><td>Mín / Máx</td><td>A faixa de "off" que cada item pode receber.</td></tr></tbody></table>

{% hint style="info" %}
Você pode forçar uma rotação da loja a qualquer momento usando \`!loja\_reset\` (apenas Moderadores/Streamer).
{% endhint %}
