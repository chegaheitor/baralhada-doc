# Dica

## ⌨️ Como usar

```
!dica <id_pacote>
```

## 📝 Descrição

Uma ajuda estratégica para completar seu álbum. O bot analisa suas cartas faltantes e dá pistas sobre uma delas em troca de alguns pontos.

## 📖 Exemplo de Resposta

> 💡 @usuario, para o pacote **Básico**, ainda faltam 3 cartas! A dica é: Rarity: Rara | Tipo: Fogo | ID: `c_r_a` | Keywords: chamas, voar, escamas

<details>

<summary>Mensagens Relacionadas</summary>

| Chave             | Quando dispara                                            |
| ----------------- | --------------------------------------------------------- |
| `hint_success`    | Quando a dica é gerada e os pontos são cobrados.          |
| `hint_fail_funds` | Se você não tiver pontos suficientes para comprar a dica. |
| `hint_fail_empty` | Se você já completou 100% daquela coleção.                |

</details>

{% hint style="info" %}
Use as `keywords` (palavras-chave) e o `maskedId` para tentar descobrir qual é a carta no seu Álbum!
{% endhint %}
