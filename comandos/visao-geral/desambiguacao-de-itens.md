# Desambiguação de Itens

## 🧠´O Problema

O Baralhada Bot permite que tanto cartas quanto pacotes tenham nomes semelhantes. Quando um comando como `!comprar` ou `!vender` é usado com um nome que corresponde **tanto a uma carta quanto a um pacote**, o bot não sabe qual você quer e precisa perguntar.

## Como Funciona

Quando isso acontece, o bot responde com a mensagem `slug_ambiguity`, por exemplo:

```
⚠️ "carta_especial" encontrado em CARTA e PACOTE. Responda com !sou_carta ou !sou_pacote para continuar.
```

O bot guarda sua resposta em andamento e continua a ação com o item correto.

## Resolvendo a Ambiguidade

| Comando       | Significado                         |
| ------------- | ----------------------------------- |
| `!sou_carta`  | Confirma que você quer a **carta**  |
| `!sou_pacote` | Confirma que você quer o **pacote** |

## Comandos que podem disparar desambiguação

* `!comprar`
* `!vender`
* `!troca`
* `!presentar`
* `!dar`
* `!remover`

{% hint style="info" %}
Como Evitar: use o **slug exato** do item como argumento. O slug é o identificador único (sem espaços, minúsculo), visível no Painel Admin ao editar a carta ou pacote.
{% endhint %}

**Exemplo:** Se a carta se chama "Carta Rara" e o slug é `carta_rara`, use:

```bash
!comprar carta_rara
```
