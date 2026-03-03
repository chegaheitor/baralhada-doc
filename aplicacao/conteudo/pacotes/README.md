# Pacotes

## 📦 O que é um Pacote

Os pacotes são os recipientes que contêm suas cartas colecionáveis. Eles definem a "loteria" da sua stream, controlando desde a raridade das cartas até a forma como os viewers competem para obtê-los.

## 🔢 Criando um Pacote

{% stepper %}
{% step %}
### Vá em **Painel → Pacotes**.

A base das suas cartas estão aqui, sem pacote, sem carta.
{% endstep %}

{% step %}
### Crie um novo pacote

Clique em **Novo Pacote**.
{% endstep %}

{% step %}
### Preencha os campos

Complete os campos do formulário conforme abaixo:

| Campo                   | Descrição                                                        |
| ----------------------- | ---------------------------------------------------------------- |
| **Nome**                | Identificação do pacote                                          |
| Slug                    |                                                                  |
| **Imagem**              | Arte de capa do pacote                                           |
| **Cartas por Pacote**   | Quantas cartas saem ao abrir (padrão: 3)                         |
| **Chances de Raridade** | Probabilidade (%) de cada raridade                               |
| **Cartas Permitidas**   | Filtro de quais cartas podem sair; vazio = todas                 |
| **Tipo de Sorteio**     | `fastest` (mais rápido) ou `raffle` (sorteio)                    |
| **% do Raffle**         | Porcentagem de participantes que ganham em modo sorteio          |
| **Limite do Fastest**   | Quantidade de viewers que podem resgatar antes de esgotar        |
| **Duração do Spawn**    | Segundos que o spawn fica disponível no chat                     |
| **Mensagem de Spawn**   | Texto customizado quando o pacote spawna no chat                 |
| **Chance de Spawn**     | Porcentagem que o pacote pode ser escolhido para spawn no evento |
| **Ativo**               | Disponível no jogo                                               |
{% endstep %}
{% endstepper %}

## 🆔 Nome do Pacote

Nome exibido no overlay e no chat quando um pacote é dropado ou aberto.

* **Exemplo**: `Pacote Místico`, `Edição Especial #01`.
* **Impacto**: Define a identidade do "drop". Um nome chamativo como "Pacote Ancestral" gera mais hype que "Pacote 1".

## 🔗 Slug (ID Amigável)

O identificador único usado nos comandos `!abrir <slug>` e `!comprar <slug>`.

O slug é gerado automaticamente a partir do nome (espaços viram `_`, caracteres especiais removidos). Pode ser editado manualmente. Deve ser único entre todas as cartas. Exemplo: "Pacote Especial" → `pacote_especial`.

* **Impacto**: Afeta diretamente a usabilidade. Se o slug for `pacote_mais_que_ultra_especial`, o viewer terá dificuldade de digitar.

## 🖼️ Imagem

A representação visual do pacote (geralmente uma caixa ou envelope) que aparece no overlay de spawn e de abertura.

* **Impacto**: É a primeira coisa que o viewer vê no overlay de spawn. Uma arte bonita aumenta a percepção de valor do item.
* **Dica**: Use PNGs com transparência para um visual mais integrado.

## 🃏 Cartas por Pacote

## 🎲 Chances de Raridade

Diferente de sistemas que sorteiam tudo de uma vez, o Baralhada Bot utiliza o **Método de Cascata** para selecionar a raridade de cada carta que sai no pacote.

#### Como funciona:

O bot realiza um teste para cada vaga de carta no pacote, seguindo esta ordem de prioridade:

1. **Checagem Lendária**: O bot roda um dado. Se cair dentro da sua % de chance, a vaga é preenchida.
2. **Checagem Épica**: Se a Lendária falhou, ele testa a % Épica.
3. **Checagem Rara**: Se a anterior falhou, ele testa a % Rara.
4. **Checagem Incomum**: Se todas falharam, resta a % Incomum.
5. **Fallback (Comum)**: Se nenhum dos testes anteriores passou, o bot entrega uma carta **Comum** automaticamente.

* **Impacto**: Isso garante que você tenha controle total sobre a escassez de itens valiosos. Se você colocar 1% para Lendária, o bot sempre tentará "acertar" esse 1% antes de desistir para as outras raridades.
* **Dica**: Este método valoriza muito as chances de cartas raras. 1% de chance Lendária em cascata é muito mais valioso que em um sorteio único de 100 itens.

## 🎰 Sistemas de Resgate&#x20;

Define como os viewers interagem com o pacote quando ele aparece na tela (Spawn).

#### ⚡ Rápido (Fastest)

O clássico "quem digitar primeiro leva".

* **Limites do Fastest**: Você define quantos pacotes estão disponíveis naquele drop. Se o limite for `1`, apenas a primeira pessoa ganha. Se o limite for `5`, as 5 pessoas mais rápidas ganham.
* **Vantagem**: Gera um senso de urgência e recompensa os viewers que estão prestando mais atenção na live.

#### 🎟️ Sorteio (Raffle)

Democrático. Todos que digitarem `!claim` no tempo estipulado entram em uma lista de espera.

* **% do Raffle**: Ao final do tempo, o bot sorteia a quantidade definida de vencedores. A chance de ganhar é igual para todos que participaram.
* **Impacto**: Ideal para comunidades grandes, garantindo que quem tem maior latência (lag) ainda tenha chance de ganhar.

## 🕒 **Duração do Spawn**

Quanto tempo (em segundos) o pacote fica "ativo" na tela aceitando comandos `!resgatar`.

* **Impacto**: Define a janela de oportunidade para os viewers interagirem com o drop antes que ele desapareça.

## **🗨 Mensagem do Spawn**

O texto personalizado que o bot envia no chat para avisar do drop.&#x20;

* **Engajamento**: Experimente usar textos diferentes para tornar a mensagem mais dinâmica e única.

## **💯 Chance de Spawn**

A probabilidade (0 a 100%) de esse pacote ser o escolhido quando o timer de drop disparar.

* **Dica**: Pacotes com cartas melhores devem ter uma chance de spawn menor para manter a economia equilibrada.

## 🃏 Cartas por Pacote

Define a quantidade de cartas que o viewer recebe ao abrir o item (ex: 1, 3 ou 5).

* **Dica**: Pacotes com mais cartas são vistos como "Premium" e geralmente custam mais caro na loja.

## ✅ Cartas Permitidas

Aqui você pode filtrar quais cartas específicas podem cair neste pacote.

* **Uso**: Ideal para criar "Pacotes de Tipo Fogo" ou "Pacotes Promocionais" que contêm apenas uma seleção restrita de cartas. Se deixado vazio, o pacote sorteará qualquer carta ativa que respeite a raridade sorteada.
* **Origem**: As opções são preenchidas automaticamente com as cartas criadas na página de **Cartas**.

{% hint style="info" %}
**Consistência é a Chave**: Tente manter um padrão entre a imagem do pacote e as cartas que ele contém. Um pacote de gelo deve, preferencialmente, conter cartas de gelo!
{% endhint %}
