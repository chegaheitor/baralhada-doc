# Comprar

## ⌨️ Como usar

```
!comprar <id_item>
```

## 📝 Descrição

Adquira novos itens diretamente da loja oficial do streamer usando seus pontos acumulados.

## 📖 Exemplo de Resposta

> 🛒 @usuario, você comprou o item **Pacote Básico** com sucesso por 1.000 pontos!

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                        | Quando dispara                                                         |
| ---------------------------- | ---------------------------------------------------------------------- |
| `buy_success`                | Confirmando a compra bem-sucedida do item.                             |
| `buy_fail_funds`             | Quando você não tem pontos suficientes para a compra.                  |
| `error_store_item_not_found` | Quando o item solicitado não existe ou não está à venda.               |
| `item_not_buyable`           | Quando o item existe no sistema mas o streamer não permitiu sua venda. |
| `slug_ambiguity`             | Se o nome digitado servir tanto para uma carta quanto para um pacote.  |

</details>

{% hint style="info" %}
* O item precisa estar marcado como **"Comprável"** no painel
* O usuário precisa ter pontos suficientes — veja saldo com [`!pontos`](../interacoes/pontos.md)
{% endhint %}

## Ambiguidade de Slug

Se o nome do item corresponder tanto a uma carta quanto a um pacote, o bot pedirá que você especifique com `!sou_carta` ou `!sou_pacote`.
