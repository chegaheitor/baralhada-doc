# Adicionar e Remover Carta/Pacote

## ⌨️ Como usar

```
!dar @usuario <carta/pacote> <id_item>
```

## 📝 Descrição

Ferramenta de injeção direta de itens. Adiciona uma carta ou pacote ao inventário de um viewer sem custos.

## 📖 Exemplo de Resposta

> 🎁 @moderador deu o item **Lendário** para @usuario!

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                        | Quando dispara                                         |
| ---------------------------- | ------------------------------------------------------ |
| `admin_inventory_add`        | Confirma o recebimento do item pelo usuário alvo.      |
| `admin_error_item_not_found` | Quando o ID do item selecionado não existe no sistema. |

</details>

{% hint style="info" %}
Não é obrigatório especificar se é `carta` ou `pacote`, caso tenha desambiguação por slugs identicos o bot avisará para escolher qual você deseja.
{% endhint %}

***

## ⌨️ Como usar

```
!remover @usuario <carta/pacote> <id_item>
```

## 📝 Descrição

Remova um item específico do inventário de um espectador. Útil para estornos ou remoção de duplicatas por erro.

## 📖 Exemplo de Resposta

> 🗑️ O item **Comum** foi removido do inventário de @usuario.

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                         | Quando dispara                                                   |
| ----------------------------- | ---------------------------------------------------------------- |
| `admin_inventory_remove`      | Confirma que o item foi retirado com sucesso da conta.           |
| `admin_error_inventory_empty` | Se o usuário não tiver aquele item específico para ser removido. |

</details>

{% hint style="danger" %}
Esta ação é irreversível e remove o item permanentemente do banco de dados do usuário.
{% endhint %}
