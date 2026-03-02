# Bloquear e Desbloquear

## ⌨️ Como usar

```
!bloquear @usuario
```

## 📝 Descrição

Bloqueia um usuário do sistema de TCG. O usuário não poderá usar comandos ou resgatar pacotes até ser desbloqueado.

## 📖 Exemplo de Resposta

> 🚫 @usuario foi bloqueado do sistema de cartas pela administração.

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                      | Quando dispara                                                        |
| -------------------------- | --------------------------------------------------------------------- |
| `admin_user_block`         | Notifica que o bloqueio foi aplicado com sucesso.                     |
| `user_blocked_interaction` | Mensagem enviada se o usuário bloqueado tentar usar comandos no chat. |

</details>

{% hint style="info" %}
O bloqueio é persistente e impede que o usuário participe de qualquer interação com o bot.
{% endhint %}

***

## ⌨️ Como usar

```
!desbloquear @usuario
```

## 📝 Descrição

Restaura o acesso de um usuário ao bot após ele ter sido bloqueado.

## 📖 Exemplo de Resposta

> ✅ O acesso de @usuario ao sistema de cartas foi restaurado.

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                | Quando dispara                                                  |
| -------------------- | --------------------------------------------------------------- |
| `admin_user_unblock` | Confirma no chat que o usuário pode voltar a jogar normalmente. |

</details>

{% hint style="info" %}
O usuário recupera todas as cartas e pontos que já possuía antes de ser bloqueado.
{% endhint %}
