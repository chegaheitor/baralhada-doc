# 🎯 Missões

## 🎯 O que são Missões

Missões são objetivos com condições e recompensas. Os usuários progridem automaticamente quando realizam ações no chat, e ao completar uma missão recebem a recompensa configurada.

## Criando uma Missão

{% stepper %}
{% step %}
### Vá em Painel → Missões

Veja todo o painel de missões&#x20;
{% endstep %}

{% step %}
### Criar nova missão

Clique em **Nova Missão**
{% endstep %}

{% step %}
### Configurar a missão

Preencha os campos abaixo:

| Campo                 | Descrição                                 |
| --------------------- | ----------------------------------------- |
| **Nome**              | Título da missão                          |
| **Descrição**         | Texto explicativo                         |
| **Tipo de Objetivo**  | Tipo de objetivo (ver tabela abaixo)      |
| **Meta Quantitativa** | Valor alvo (ex: 5 para "abrir 5 pacotes") |
| **Recompensa**        | Pontos, cartas ou pacotes                 |
| **Recorrência**       | Tempo de repetição da missão              |
| **Ativa**             | Se aparece para os usuários               |
{% endstep %}
{% endstepper %}

## 🎯 Tipos de Missão

<table><thead><tr><th width="268">Tipo de Objetivo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>💬 Mensagens (Chat)</strong></td><td>Monitora a participação ativa do usuário no chat.</td></tr><tr><td><strong>📦 Abrir Pacotes</strong></td><td>Conta a abertura de qualquer pacote de cartas.</td></tr><tr><td><strong>🃏 Coletar Cartas</strong></td><td>Focado na obtenção de novas cartas (geralmente por raridade).</td></tr><tr><td><strong>🎯 Cartas Específicas</strong></td><td>Exige que o usuário consiga cartas específicas da coleção.</td></tr><tr><td><strong>📁 Pacotes Específicos</strong></td><td>Conta apenas a abertura de pacotes de uma coleção definida.</td></tr><tr><td><strong>🛒 Comprar Pacotes</strong></td><td>Registra compras de pacotes na loja oficial.</td></tr><tr><td><strong>💰 Vender Pacotes</strong></td><td>Monitora a venda de pacotes pelo usuário.</td></tr><tr><td><strong>🏪 Comprar Cartas</strong></td><td>Registra a compra de cartas individuais no mercado ou loja.</td></tr><tr><td><strong>💵 Vender Cartas</strong></td><td>Monitora a venda de cartas individuais.</td></tr><tr><td><strong>🤝 Trocas Realizadas</strong></td><td>Incentiva a interação social através de trocas concluídas.</td></tr><tr><td><strong>🎁 Presentes Enviados</strong></td><td>Recompensa o envio de itens para outros membros da comunidade.</td></tr><tr><td><strong>🔨 Manual (Admin)</strong></td><td>Missões personalizadas que são validadas manualmente pela equipe.</td></tr></tbody></table>

## 📊 Progresso Automático

O progresso é atualizado automaticamente cada vez que o usuário realiza a ação correspondente ao tipo da missão. Os usuários podem ver seu progresso com [`!mission`](file:///2776789/comandos/mission.md).

## 🎁 Recompensas

As recompensas são as mais variadas, configure o que o usuário recebe ao completar a missão de acordo com a complexidade da missão:

* **Pontos:** valor numérico de pontos
* **XP:** valor numério de xp
* **Carta:** ID de uma carta específica
* **Pacote:** ID de um pacote específico

## 🤖 Funcionamento no Bot

O bot monitora todas as ações em tempo real:

#### Comandos de Chat

* `!missao`: Exibe a lista de missões disponíveis para o usuário e o seu progresso atual (ex: `Mensagens: 40/50`).
* **Alertas Automáticos**: Assim que a meta é batida, o bot envia uma mensagem celebrando a vitória e confirmando o recebimento dos pontos/XP.

## 💡 Estratégia e Impactos

* **Impacto no Engajamento**: Missões de "Mensagens" aumentam a retenção e o volume do chat, o que ajuda no algoritmo da Twitch.
* **Impacto na Economia**: Use as missões para injetar pontos na economia de forma controlada, sem depender apenas do tempo de visualização.

{% hint style="info" %}
Mantenha as missões diárias fáceis! Isso garante que o viewer se sinta recompensado logo no início da stream, aumentando as chances de ele permanecer na live para tentar objetivos mais difíceis.
{% endhint %}

## 📊 Visualizar Progresso

É possivel visualizar o progresso de cada missão individualmente, para ver quais usuários ja completou e quais estão quase lá!

{% hint style="danger" %}
Se você deletar uma missão, todo o progresso dos usuários nela será removido permanentemente. Prefira editar ou desativar em vez de excluir.
{% endhint %}
