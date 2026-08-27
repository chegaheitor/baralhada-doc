# 🗣️ Fala

## TERMINAR DE CONFIGURAR A PAGINA

## ⌨️ Como usar

```
!fala <id_carta> <mensagem>
```

## 📝 Descrição

O comando permite que os espectadores conversem diretamente com as cartas do seu deck ativo. A IA assume a personalidade da carta solicitada e responde às asneiras, perguntas ou cantadas dos seus viewers em tempo real.

## 📖 Exemplo de Resposta

> _Eu sou um Dragão do Caos de 8000 de Ataque, {Viewer}, as chamas do abismo correm nas minhas veias. Acha mesmo que eu me importo com seus doces humanos macios? (Mas se você tiver um pedaço de cavaleiro torrado, eu aceito)._

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
