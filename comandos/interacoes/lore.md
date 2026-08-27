# 📜 Lore

## TERMINAR DE CRIAR

## ⌨️ Como usar

```
!lore <id_carta>
```

## 📝 Descrição

O comando integra a IA junto com a descrição e informações da carta, para gerar um pequeno texto de lore dela para os usuários.

## 📖 Exemplo de Resposta

> _Ah, jovem aventureiro... puxe um banquinho e me escute bem de perto. Dizem que o {Escudo de Prata} era usado pelos simples guardas da capital, como peças {Comuns} forjadas às pressas. Mas poucos sabem que durante o grande cerco da {Coleção Cidadão}, o prateado desses escudos foi a única luz refletindo a velha lua sangrenta que impediu as tropas mortas-vivas de atravessarem os portões. O poder de pura {Defesa} estava banhado de coragem de camponeses que nunca retornaram._

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
