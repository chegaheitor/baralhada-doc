# 🕵️ Dica

## ⌨️ Como usar

```
!dica <id_pacote>
```

## 📝 Descrição

Uma ajuda estratégica para completar seu álbum. O bot analisa suas cartas faltantes e dá pistas sobre uma delas em troca de alguns pontos.

## 📖 Exemplo de Resposta

> 💡 @usuario, para o pacote **Básico**, ainda faltam 3 cartas! A dica é: Rarity: Rara | Tipo: Fogo | ID: `c_r_a` | Keywords: chamas, voar, escamas

<details>

<summary>Mensagens Relacionadas</summary>

| Chave             | Quando dispara                                            |
| ----------------- | --------------------------------------------------------- |
| `hint_success`    | Quando a dica é gerada e os pontos são cobrados.          |
| `hint_fail_funds` | Se você não tiver pontos suficientes para comprar a dica. |
| `hint_fail_empty` | Se você já completou 100% daquela coleção.                |

</details>

{% hint style="info" %}
Use as `keywords` (palavras-chave) e o `maskedId` para tentar descobrir qual é a carta no seu Álbum!
{% endhint %}

## 🔍 Como funciona o `!dica`

Quando um usuário usa o comando `!dica <id_pacote>`, o bot:

1. Verifica quais cartas daquele pacote o usuário ainda **não possui**.
2. Sorteia uma dessas cartas faltantes como alvo.
3. Gera um relatório misterioso no chat.

## 🎭 Mascaramento de ID e Slugs

Para não revelar o ID exato da carta (o que permitiria a compra direta), o bot aplica um **mascaramento de 60%**:

* Exemplo: Se o ID for `charizard_fire`, o bot pode exibir `ch_r_z_rd_f_r_`.
* Isso força o usuário a adivinhar ou pesquisar na lore.

#### 🧠 Extração de Palavras-Chave

O bot analisa a **Descrição (Lore)** da carta e extrai aleatoriamente 3 palavras significativas (com mais de 4 letras) para servir de pista textual.

* Exemplo: "Este dragão vive em **montanhas** e adora **fogo** intenso." -> Pistas: _Montanhas, Fogo, Intenso_.

### 🔥 Hype de Coleção

O sistema de pistas detecta o quão perto o usuário está de completar o álbum e adiciona mensagens automáticas de incentivo:

* **Faltam 1-3 cartas:** "(TÁ CHEGANDO A HORA! 🔥)"
* **Falta apenas 1 carta:** "(ESTÁ QUASE ACABANDO! 😱)"
