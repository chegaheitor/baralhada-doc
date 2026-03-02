# Troca Oferta

## ⌨️ Como usar

```
!trocaoferta <id_item>
```

## 📝 Descrição

Responda a uma proposta de troca iniciada por outro usuário, oferecendo um item do seu inventário de volta.

## 📖 Exemplo de Resposta

> 🔄 @usuario ofereceu **Escudo de Prata** na troca. @proponente, você aceita? (!trocasim para confirmar)

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                  | Quando dispara                                                        |
| ---------------------- | --------------------------------------------------------------------- |
| `trade_offer_made`     | Quando o segundo participante define qual item quer dar em troca.     |
| `trade_error_no_trade` | Se você tentar oferecer um item sem ter uma troca iniciada para você. |
| `trade_error_item`     | Se você não possuir o item que está tentando oferecer.                |

</details>

{% hint style="info" %}
Após você fazer a oferta, o proponente inicial deve usar `!trocasim` para finalizar o negócio. Ou `!trocanao` para negar a troca.
{% endhint %}

***

## ⌨️ Como usar

```
!trocasim
```

## 📝 Descrição

Confirme e finalize a negociação. Este comando transfere os itens entre as contas e encerra a sessão de troca com sucesso.

## 📖 Exemplo de Resposta

> ✅ Troca concluída! @usuarioA recebeu **Mago** e @usuarioB recebeu **Guerreiro**.

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                  | Quando dispara                                                                 |
| ---------------------- | ------------------------------------------------------------------------------ |
| `trade_success`        | Quando a troca é finalizada com sucesso.                                       |
| `trade_error_no_offer` | Se você tentar confirmar sem que o outro usuário tenha feito uma oferta ainda. |

</details>

{% hint style="info" %}
Apenas o usuário que **iniciou** a troca pode usar o `!trocasim` para aceitar a contra-proposta do parceiro.
{% endhint %}

***

## ⌨️ Como usar

```
!trocanao
```

## 📝 Descrição

Cancele imediatamente uma negociação de troca em andamento. Qualquer um dos dois participantes pode usar este comando a qualquer momento.

## 📖 Exemplo de Resposta

> 🛑 A troca foi cancelada por @usuario.

<details>

<summary>Mensagens Relacionadas</summary>

| Chave            | Quando dispara                          |
| ---------------- | --------------------------------------- |
| `trade_canceled` | Quando a troca é encerrada sem sucesso. |

</details>

{% hint style="info" %}
Use este comando se você mudar de ideia ou se a contra-proposta do outro usuário não for interessante.
{% endhint %}
