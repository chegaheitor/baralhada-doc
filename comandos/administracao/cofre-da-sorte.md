# 🍀 Cofre da Sorte

## 🔒 Cofre da Sorte

## ⌨️ Como usar

```
!participar
```

## 📝 Descrição

O **Cofre da Sorte** é um evento especial de spawn que pode aparecer aleatoriamente no chat. O cofre cobra um preço para ser aberto, os usuários que participarem adicionam uma carta ao cofre, e apenas um abre o cofre e leva todas as cartas.

## 📖 Exemplo de Resposta

> **Usuário:** `!participar` **Bot:** `✅ @usuario, você entrou no sorteio do Cofre da Sorte!`

> **Bot (Resultado):** `🏆 @vencedor abriu o cofre e ganhou o prêmio! Parabéns!`

## 🔢 Fluxo do Evento

1. **Alerta:** Um overlay especial aparece avisando que um Cofre da Sorte está no chat.
2. **Participação:** Os usuários devem digitar `!participar` dentro do tempo limite.
3. **Sorteio:** Após o tempo expirar, o bot escolhe um vencedor aleatório entre os participantes.
4. **Premiação:** O vencedor recebe o conteúdo do cofre (cartas) e um overlay de comemoração é exibido.

## ⚙️ Configuração

Você pode ativar a chance de um spawn se tornar um **Cofre da Sorte** através do painel de **Spawns**:

* Ao criar ou editar um spawn, marque a opção "Cofre da Sorte".
* Defina a porcentagem de chance de o cofre aparecer em vez do pacote padrão.

<details>

<summary>Mensagens Relacionadas</summary>

| Chave               | Quando dispara                                          |
| ------------------- | ------------------------------------------------------- |
| `event_cofre_start` |                                                         |
| `event_joined`      |                                                         |
| `cofre_start`       | Quando o cofre aparece no chat e no overlay.            |
| `cofre_winner`      | Quando o sorteio acaba e um vencedor é anunciado.       |
| `cofre_entry`       | Mensagem confirmando que o usuário entrou no sorteio.   |
| `cofre_no_entry`    | Mensagem se o tempo acabar e ninguém tiver participado. |

</details>

{% hint style="success" %}
O Cofre da Sorte é uma excelente ferramenta para gerar "hype" e garantir que o público esteja prestando atenção na stream!
{% endhint %}
