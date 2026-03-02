# Troca

## ⌨️ Como usar

```
!troca @usuario <seu_item>
```

## 📝 Descrição

Inicie uma negociação segura com outro espectador. Este comando abre uma sessão de troca onde ambos podem oferecer itens antes de confirmar.

## 📖 Exemplo de Resposta

> 🤝 @usuario propôs uma troca para @alvo: oferece **Espada Comum**. Aguardando contra-oferta...

<details>

<summary>Mensagens Relacionadas</summary>

| Chave              | Quando dispara                                             |
| ------------------ | ---------------------------------------------------------- |
| `trade_initiated`  | Quando a proposta inicial é enviada com sucesso.           |
| `trade_offer_made` | Quando a outra pessoa responde com o item dela.            |
| `trade_success`    | Quando ambos confirmam e a troca de itens é realizada.     |
| `trade_canceled`   | Quando um dos usuários cancela ou o tempo da troca expira. |

</details>

{% hint style="info" %}
Para completar a troca, o outro usuário deve usar `!trocaoferta <item>` e o iniciador deve finalizar com `!trocasim` ou negar a contra-proposta com `!trocanao`
{% endhint %}

***

### Fluxo Completo

{% stepper %}
{% step %}
### Usuário A inicia a proposta

Usuário A:

```
!trade @UsuarioB dragao_de_fogo
```

Bot notifica o destinatário:

```
@UsuarioB, usuarioA quer trocar dragão_de_fogo com você! Use !tradeOffer aceitar ou recusar.
```
{% endstep %}

{% step %}
### Usuário B responde

UsuarioB:

```
!tradeOffer aceitar
```

Bot confirma:

```
✅ Troca realizada com sucesso!
```
{% endstep %}
{% endstepper %}

***

{% hint style="info" %}
A proposta tem um tempo limite. Se não houver resposta dentro do prazo, a troca é cancelada automaticamente.
{% endhint %}
