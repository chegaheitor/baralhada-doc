# 🎨 Personalização

## 💎 O que são Raridades e Tipagens

* **Raridades**: Definem a escassez, a cor da borda e o brilho da carta no overlay.
* **Tipagens (Tags)**: Atributos textuais/ícones que classificam as cartas (ex: Elementos, Classes, Categorias).

### 🛠️ Criando uma Raridade

{% stepper %}
{% step %}
## Vá em Painel → Personalização → Raridades

Aqui você define a hierarquia de valores do seu jogo.
{% endstep %}

{% step %}
## Preencha as propriedades

<table><thead><tr><th width="150">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nome</strong></td><td>Ex: "Lendária", "Holográfica", "Mística".</td></tr><tr><td><strong>Cor (Hex)</strong></td><td>O código da cor que aparecerá na borda (ex: #FFD700).</td></tr><tr><td><strong>Ordem (Drop)</strong></td><td>Usado para o cálculo de drop das cartas na abertura de pacotes</td></tr></tbody></table>
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Uma boa escolha de cores hexadecimais faz seu overlay parecer um jogo profissional Triple-A.
{% endhint %}

***

## 🏷️ Criando uma Tipagem (Tipos)

{% stepper %}
{% step %}
## Vá em Painel → Personalização → Tipagens

Defina os ícones e elementos do seu sistema.
{% endstep %}

{% step %}
## Configurar Tipagem

<table><thead><tr><th width="150">Campo</th><th width="532">Descrição</th></tr></thead><tbody><tr><td><strong>Nome do Tipo</strong></td><td>Ex: Fogo, Água, Tanker, Suporte.</td></tr><tr><td><strong>Ícone/Emoji</strong></td><td>O caractere ou emoji que o bot usará no chat.</td></tr><tr><td><strong>Cor do Texto</strong></td><td>Como o nome do tipo aparecerá nos menus.</td></tr></tbody></table>
{% endstep %}
{% endstepper %}

{% hint style="info" %}
As tipagens não influenciam em nada as cartas, mas é legal ter uma identidade visual para cada uma, o Pikachu não seria ele se não fosse de raio!
{% endhint %}

## 🎰 O Peso do Drop (Raridade)

Controla matematicamente a sorte do seu chat.

* **Impacto**: Se você tiver muitas raridades com peso baixo, sua live será "generosa". Pesos baixos tornam o jogo "hardcore".
* **Regra de Ouro**: A raridade "Comum" deve ter o maior peso de todos para servir de base econômica.

## 🏷️ Categorização (Tipos)

* **Vantagem**: Ajuda na criação de filtros na loja e facilita a busca por cartas específicas.
* **Dica**: Não crie tipos demais (ex: 50 tipos). Tente manter entre **5 e 15** tipos principais para facilitar a memorização dos viewers.
* **Mais de 1 tipo:** É possivel ter até 2 tipos por carta, pense em fazer misturas com a tipagem para cada carta ser única.
