# ✅ Resgatar

## ⌨️ Como usar

```
!resgatar
```

## 📝 Descrição

O comando fundamental para coletar os pacotes spawnados no chat. Use para resgatar pacotes que "dropam" no chat através do sistema de spawns automáticos ou manuais.

## 📖 Exemplo de Resposta

> 🎉 @usuario resgatou o pacote Épico com sucesso!

<details>

<summary>Mensagens Relacionadas</summary>

| Chave           | Quando dispara                                                                             |
| --------------- | ------------------------------------------------------------------------------------------ |
| `claim_success` | Quando você é o primeiro a resgatar (em modo Rápido) ou entra no sorteio (em modo Raffle). |
| `claim_full`    | Quando o estoque do pacote que dropou já acabou.                                           |
| `no_spawn`      | Quando você usa !claim mas não há nenhum pacote ativo no momento.                          |
| `raffle_entry`  | Mensagem específica confirmando que você entrou na lista do sorteio.                       |

</details>

{% hint style="info" %}
Fique atento ao **Overlay**! O alerta visual geralmente aparece um pouco antes do chat e te dá a vantagem de digitar `!resgatar` primeiro.
{% endhint %}

## 📦 Tipo de resgate

#### Tipo "Fastest" (Mais Rápido)

O **primeiro usuário** a digitar `!resgatar` fica com o item. Os outros recebem uma mensagem de falha.

#### Tipo "Raffle" (Sorteio)

Todos os usuários que digitarem `!resgatar` durante a janela de tempo entram em um sorteio. Uma porcentagem configurável de participantes ganha.

{% hint style="warning" %}
Configuração do tipo de claim, duração e porcentagem do sorteio é feita por pacote no Painel Admin → Pacotes.
{% endhint %}
