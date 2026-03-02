# Usuarios

## 👤 O que é o Gerenciamento de Usuários

A página de Usuários mostra todos os viewers que já interagiram com o bot. O sistema permite que você visualize o progresso de cada viewer, ajuste seus pontos, cartas e pacotes manualmente, ou aplique bloqueios em casos de abuso do sistema.

{% stepper %}
{% step %}
### Vá em Painel → Usuários

Acesse a lista completa de todos que já interagiram com o bot na sua live.
{% endstep %}

{% step %}
### Busque o Usuário

Utilize a barra de pesquisa para encontrar o viewer pelo nome de usuário da Twitch.
{% endstep %}

{% step %}
### Gerenciar Ações

Ao selecionar um usuário, você pode abrir o formulário de edição:

<table><thead><tr><th width="150">Ação</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Editar Saldo</strong></td><td>Adicionar ou remover pontos diretamente da carteira do usuário.</td></tr><tr><td><strong>Editar Nível/XP</strong></td><td>Adicionar ou remover níveis/xp diretamente pro painel do usuário.</td></tr><tr><td><strong>Ver Inventário</strong></td><td>Visualizar todas as cartas e pacotes que o usuário possui em sua mochila.</td></tr><tr><td><strong>Ver Álbum</strong></td><td>Visualizar os álbuns do usuario e ver sua coleção de cartas.</td></tr><tr><td><strong>Ver Conquistas/Missões</strong></td><td>Visualizar todas as conquistas desbloqueadas e progresso de missões do usuário.</td></tr><tr><td><strong>Dar Item</strong></td><td>Enviar uma carta ou pacote específico para o usuário.</td></tr><tr><td><strong>Banir/Bloquear</strong></td><td>Impedir que o usuário use qualquer comando do bot.</td></tr><tr><td><strong>Limpar Progresso</strong></td><td>Limpar todo o histórico, nível e inventário (irreversível).</td></tr></tbody></table>
{% endstep %}
{% endstepper %}

## 💰 Editar Saldo (Pontos)

Permite ajustes finos na economia do usuário. É possivel adicionar ou remover pontos.&#x20;

* **Impacto**: Útil para premiar vencedores de gincanas ou corrigir erros após uma falha de sistema.
* **Dica**: Evite dar muitos pontos manualmente para não desvalorizar o esforço dos outros jogadores.

{% hint style="warning" %}
A carteira nunca fica negativa, o menor valor de pontos é 0
{% endhint %}

## 📈 Editar Nível e XP

Permite ajustar manualmente o progresso de experiência e o nível do usuário.

* **Impacto**: Útil para restaurar o progresso de veteranos ou recompensar viewers por contribuições especiais fora da live.
* **Dica**: Lembre-se que o nível muitas vezes desbloqueia permissões ou multiplicadores automáticos no sistema.

## 🎒 Ver Inventário

O inventário mostra todas as cartas e pacotes que aquele usuário possui.

* **Visualização**: O painel mostra as artes das cartas exatamente como aparecem no álbum do usuário.

## 📖 Ver Álbum

Uma visão organizada da coleção completa do usuário, separada por álbuns/pacotes.

* **Coleção**: Permite identificar rapidamente quais cartas faltam para completar uma coleção específica ou set de pacotes.
* **Filtros**: Facilita a navegação pelo acervo do usuário, permitindo visualizar o progresso de conclusão de cada álbum separadamente.

## 🏆 Ver Conquistas e Missões

Acompanhe o engajamento do usuário através de seus marcos alcançados e objetivos atuais. É possivel ver as conquistas desbloqueadas por aquele usuário, e as missões que ele ja concluiu

* **Histórico**: Veja a lista de conquistas desbloqueadas, permitindo entender o nível de fidelidade e os grandes feitos do viewer na live.

## 🚫 Banir/Bloquear

A ferramenta definitiva de segurança. Utilize para moderar o programa de acordo com seu chat. Todo usuário bloqueado fica impossibilitado de interagir com o bot e outros usuários, como fazer trocas, receber pontos por mensagens, resgatar spawns e mais.&#x20;

* **Impacto**: O usuário parado de ser monitorado pelo bot e seus comandos são ignorados no chat.
* **Regra de Ouro**: Use apenas em casos de comportamento tóxico ou exploração de bugs (exploits).

<details>

<summary><strong>🖼 Por que a foto de perfil do usuário não aparece?</strong></summary>

Isso ocorre porque o **Client ID** e o **Client Secret** precisam estar configurados corretamente nas definições do bot. O sistema utiliza a **API Helix** da Twitch para buscar metadados como fotos de perfil; apenas o Token OAuth não é suficiente para carregar essas informações.

</details>

<details>

<summary>🚫 O banimento no painel também bane o usuário do chat da Twitch?</summary>

Não. O bloqueio no sistema apenas impede que o bot responda aos comandos do usuário e interrompe a coleta de pontos. Para banir do chat, você deve usar as ferramentas nativas da Twitch.

</details>

<details>

<summary>👤 O que acontece se o viewer mudar o nome de usuário (username) na Twitch?</summary>

Nada é perdido. O sistema utiliza o ID único da Twitch para identificar cada conta. Assim que o usuário interagir com o bot novamente, o nome será atualizado automaticamente no seu painel sem afetar o progresso.

</details>

