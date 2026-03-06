# 🤑 Apostar

## ⌨️ Como usar

```
!apostar <quantidade>
```

## 📝 Descrição

Tente a sorte e aposte seus pontos para ganhar um multiplicador sobre o valor apostado. As chances de vitória e o multiplicador são definidos pelo streamer nas configurações de economia.

## 📖 Exemplo de Resposta

> 🎉 @usuário ganhou a aposta e recebeu 1000 Pontos! (Multiplicador: 2.0x)

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                  | Quando dispara                                           |
| ---------------------- | -------------------------------------------------------- |
| `gamble_win`           | Quando o usuário vence a aposta.                         |
| `gamble_loss`          | Quando o usuário perde a aposta.                         |
| `gamble_error_funds`   | Quando o usuário não tem pontos suficientes.             |
| `gamble_error_min_max` | Quando o valor excede ou é menor que o limite permitido. |

</details>

### ⚙️ Configurações

Este comando é influenciado pelas seguintes definições na página de [**Pontos**](../../aplicacao/comunidade/pontos.md):

* **Chance de Vitória:** A probabilidade (0-100) do usuário vencer a aposta.
* **Multiplicador:** O valor pelo qual a aposta é multiplicada em caso de vitória.

{% hint style="info" %}
Dica: Ajuste a chance de vitória para manter a economia da sua live equilibrada e emocionante!
{% endhint %}
