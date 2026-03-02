# Missão

## ⌨️ Como usar

```
!missao
```

## 📝 Descrição

Acompanhe seus objetivos ativos e o quanto falta para concluí-los. Ganhe pontos e XP ao completar cada missão.

## 📖 Exemplo de Resposta

> 🎯 @usuario, suas missões: • Colecionador Iniciante: 3/5 cartas (500 pts) • Tagarela: 45/100 mensagens (200 pts)

<details>

<summary>Mensagens Relacionadas</summary>

| Chave              | Quando dispara                                                |
| ------------------ | ------------------------------------------------------------- |
| `mission_list`     | Lista todas as missões que você ainda não completou.          |
| `mission_empty`    | Quando não existem missões ativas ou você já completou todas. |
| `mission_progress` | Formato individual de cada linha de missão na lista.          |

</details>

{% hint style="info" %}
As recompensas são entregues automaticamente assim que você atinge a meta. Não é necessário comando extra para resgatar.
{% endhint %}

## 🎯 Como as Missões São Completadas

O progresso das missões é atualizado automaticamente quando o usuário realiza ações relevantes:

| Tipo de Missão           | Ação que avança o progresso            |
| ------------------------ | -------------------------------------- |
| Abrir pacotes            | `!open`                                |
| Coletar cartas via spawn | `!claim`                               |
| Gastar pontos            | `!buy`                                 |
| Completar coleção        | Coletar todas as cartas de uma coleção |

{% hint style="info" %}
Gerenciar Missões: Missões são criadas no Painel Admin → Missões.
{% endhint %}
