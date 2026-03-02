# Adicionar e Remover Pontos

## ⌨️ Como usar

```
!addpontos @usuario
```

## 📝 Descrição

Adicione saldo diretamente à carteira de um usuário. Útil para premiar viewers ou corrigir saldo manualmente.

## 📖 Exemplo de Resposta

> 💰 @moderador adicionou 1.000 pontos para @usuario. Novo saldo: 2.500 pontos.

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                        | Quando dispara                                                      |
| ---------------------------- | ------------------------------------------------------------------- |
| `admin_points_set`           | Exibe a confirmação do novo saldo do usuário após a adição.         |
| `admin_error_invalid_amount` | Quando o valor digitado não é um número válido ou é menor que zero. |
| `admin_error_user_not_found` | Quando o usuário marcado não foi encontrado no banco de dados.      |

</details>

{% hint style="info" %}
Somente Moderadores e o Streamer podem usar este comando por padrão.
{% endhint %}

***

## ⌨️ Como usar

```
!rempontos @usuario
```

## 📝 Descrição

Remova pontos do saldo de um espectador. O bot não permite valores negativos (o saldo mínimo será 0).

## 📖 Exemplo de Resposta

> 💰 @moderador removeu 500 pontos de @usuario. Saldo atual: 1.200 pontos.

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                        | Quando dispara                                     |
| ---------------------------- | -------------------------------------------------- |
| `admin_points_set`           | Exibe o novo saldo reduzido do usuário.            |
| `admin_error_invalid_amount` | Quando a quantidade de pontos digitada é inválida. |

</details>

{% hint style="info" %}
Use este comando com cautela para aplicar multas ou corrigir erros de premiação.
{% endhint %}
