# Abrir

## ⌨️ Como usar

```
!abrir <id_pacote>
```

## 📝 Descrição

O comando de "unboxing" das suas cartas. Use para abrir pacotes que você conquistou em sorteios ou comprou na loja.

## 📖 Exemplo de Resposta

> 📦 @usuario abriu o pacote Básico e encontrou: Dragão (C), Espada (C), Mago (I)

<details>

<summary>Mensagens Relacionadas</summary>

| Chave                  | Quando dispara                                                  |
| ---------------------- | --------------------------------------------------------------- |
| `pack_opened`          | Quando o pacote é aberto com sucesso e exibe as cartas.         |
| `no_packs`             | Quando você tenta abrir um pacote que não possui no inventário. |
| `error_pack_not_found` | Quando o ID do pacote digitado não existe no sistema.           |

</details>

{% hint style="info" %}
Você pode usar o comando `!mochila` para ver os IDs exatos dos pacotes que você tem antes de tentar abrir.
{% endhint %}

