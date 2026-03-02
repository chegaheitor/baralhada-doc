# Troca Manual

## O que é

A Troca Manual permite que o **administrador** transfira itens entre dois usuários diretamente pelo painel, sem precisar dos comandos do chat. Útil para:

* Corrigir erros em trocas que falharam
* Distribuir prêmios de eventos
* Ajustar inventários manualmente
* Realizar trocas especiais acordadas fora do chat

## Como Usar

{% stepper %}
{% step %}
### Selecione os usuários

* Vá em **Painel → Troca Manual**
* Selecione o **Usuário A** no seletor esquerdo
* Selecione o **Usuário B** no seletor direito
{% endstep %}

{% step %}
### Carregamento dos inventários

* Os inventários de ambos são carregados automaticamente
* Use a barra de pesquisa para filtrar itens
{% endstep %}

{% step %}
### Seleção de itens

* Clique em um item para adicioná-lo à seleção
* Ajuste a quantidade com os botões `+` e `-`
{% endstep %}

{% step %}
### Confirmação

* Clique em **Confirmar Troca**
* Um modal de confirmação exibirá o resumo completo antes de finalizar
{% endstep %}
{% endstepper %}

## Interface

* **Lado esquerdo:** inventário do Usuário A (o que ele vai dar)
* **Lado direito:** inventário do Usuário B (o que ele vai dar)
* **Área central:** resumo dos itens selecionados de cada lado

Como os itens são exibidos:

* Cartas: aparecem com **imagem, nome e raridade**
* Pacotes: aparecem com **imagem e quantidade disponível**

## Confirmação

Antes de realizar a troca, um modal de confirmação exibe o resumo completo:

```
Usuário A (chegaheitor): 1x Dragão de Fogo
Usuário B (amigo): 2x Pacote Básico
```

{% hint style="warning" %}
A troca é irreversível pela interface. Em caso de erro, use **Painel → Usuários** para ajustar os inventários manualmente.
{% endhint %}
