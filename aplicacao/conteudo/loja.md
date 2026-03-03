# 🛒 Loja

## 🛒 Como Funciona a Loja

A Loja é o centro econômico do seu bot. Ela permite que os viewers invistam os pontos ganhos na live para adquirir itens específicos ou recuperem pontos ao venderem cartas repetidas. Ela é montada automaticamente a partir das cartas e pacotes criados nas páginas anteriores.

## 💰 Configuração de Preços

Ao gerenciar Cartas ou Pacotes, você encontrará dois campos financeiros principais:

#### 📥 Preço de Compra

O valor em pontos que o usuário deve pagar para adquirir o item.

* **Impacto**: Define a barreira de entrada para itens raros. Preços muito altos podem desencorajar novos players, enquanto preços muito baixos podem inflacionar a economia.
* **Comando**: Afeta o funcionamento do `!comprar <slug>`.

#### 📤 Preço de Venda

O valor em pontos que o bot devolve ao usuário quando ele decide se desfazer do item.

* **Impacto**: É a principal forma de "reciclagem" de cartas repetidas. Permite que o viewer continue jogando mesmo sem ganhar spawns.
* **Comando**: Afeta o funcionamento do `!vender <slug>`.

## ⚙️ Controle de Disponibilidade

Nem todo item criado precisa estar circulando na economia. Você controla isso através de dois "toggles" (chaves):

| Configuração  | Descrição                                                | Impacto                                                                                |
| ------------- | -------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **Comprável** | Ativa a possibilidade de comprar o item na loja pública. | Se desativado, o item só pode ser obtido via **Spawn** ou comandos de Admin.           |
| **Vendível**  | Permite que o bot aceite o item de volta.                | Se desativado, o viewer fica com o item permanentemente (ou deve trocá-lo com outros). |

## 🔍 Filtros e Busca

Facilite a navegação usando os filtros por:

* **Coleção**: Ver itens de um álbum específico.
* **Raridade**: Filtrar apenas Lendárias, Raras, etc.
* **Tipo de Item**: Alternar entre ver apenas Cartas ou apenas Pacotes.

## 📈 Margem de Valor

No Painel da Loja, você verá um indicador de porcentagem calculado automaticamente:

> **Fórmula**: `(Preço de Venda / Preço de Compra) * 100`

* **O que isso significa?**: Representa a taxa de retorno do investimento do viewer.
* **Exemplo**: Se um pacote custa **1000** e o bot paga **200** na recompra, a margem é de **20%**.
* **Dica Estratégica**:
  * **Margens Altas (50-80%)**: Incentivam o giro rápido de cartas e facilitam o progresso de novos usuários.
  * **Margens Baixas (10-30%)**: Valorizam a posse do item e tornam a compra na loja uma decisão mais estratégica e pesada.

## 🛡️ Regras de Interação

#### Ambiguidade de Nomes

Como viewers podem comprar tanto Cartas quanto Pacotes pelo mesmo comando, o sistema possui uma proteção contra erros:

* Se existir um **Pacote** chamado "Iniciante" e uma **Carta** chamada "Iniciante", o bot perguntará qual o usuário deseja.
* O usuário deve responder com `!sou_carta` ou `!sou_pacote` para confirmar a transação.

#### Restrições de Venda

* Itens que estão em uma **Sessão de Troca** ativa não podem ser vendidos até que a troca seja finalizada ou cancelada.
* O bot nunca permitirá que um usuário fique com saldo negativo.

{% hint style="info" %}
**Ajuste Fino**: Você pode usar o Painel de Estatísticas para ver quais itens são mais comprados e ajustar os preços para manter o desafio sempre interessante na sua stream!
{% endhint %}
