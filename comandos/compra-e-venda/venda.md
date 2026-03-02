# Venda

## ⌨️ Como usar

```
!vender <id_item>
```

## 📝 Descrição

Transforme seus itens repetidos ou indesejados em pontos para poder comprar novos pacotes na loja.

## 📖 Exemplo de Resposta

> 💰 @usuario, você vendeu **Mago de Fogo** e recebeu 150 pontos!

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                   | Quando dispara                                                       |
| ----------------------- | -------------------------------------------------------------------- |
| `sell_success`          | Confirmando que a venda foi realizada e os pontos foram adicionados. |
| `inventory_error`       | Quando você tenta vender algo que não possui no seu deck/mochila.    |
| `error_item_not_exists` | Quando o ID do item digitado é inválido.                             |
| `item_not_sellable`     | Quando o streamer desativou a venda desse item específico.           |

</details>

{% hint style="info" %}
* O item precisa estar marcado como **"Comprável"** no painel
* O usuário precisa ter pontos suficientes — veja saldo com [`!pontos`](../interacoes/pontos.md)
{% endhint %}

{% hint style="success" %}
Configure o preço de venda um pouco abaixo do preço de compra para criar uma diferença saudável e estimular a compra via spawn/daily ao invés de farm de loja.
{% endhint %}

## Ambiguidade de Slug

Se o nome do item corresponder tanto a uma carta quanto a um pacote, o bot pedirá que você especifique com `!sou_carta` ou `!sou_pacote`.
