# Carta

## ⌨️ Como usar

```
!carta <id_carta>
```

## 📝 Descrição

Veja os detalhes técnicos de uma carta específica, incluindo seus atributos de combate (HP, Ataque, Defesa) e sua descrição de lore.

## 📖 Exemplo de Resposta

> 🃏 **Dragão de Fogo** (#001) | Fogo 🔥 | Rara | ❤️ 100 ⚔️ 45 🛡️ 30 | Descrição: cospe chamas azuis. | Compra: 500 pts | Venda: 150 pts

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                  | Quando dispara                                                       |
| ---------------------- | -------------------------------------------------------------------- |
| `card_info`            | Exibe todos os dados da carta e aciona a inspeção visual no overlay. |
| `error_card_not_found` | Quando o ID da carta digitado não existe no banco de dados.          |

</details>

{% hint style="info" %}
Além da resposta no chat, este comando faz a carta aparecer no **Overlay** da live!
{% endhint %}
