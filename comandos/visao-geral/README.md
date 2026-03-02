# Visão Geral

O Baralhada Bot responde a comandos digitados no chat do Twitch. Todos os comandos precisam começar com `!` para ser detectado pelo bot no chat para funcionar.

***

## 🤖 Tabela de Comandos

<table><thead><tr><th width="337">Comando</th><th width="276">Descrição</th><th>Permissão padrão</th></tr></thead><tbody><tr><td><code>!resgatar</code></td><td>Pegar o spawn ativo no chat</td><td>Viewer</td></tr><tr><td><code>!abrir</code></td><td>Abrir um pacote do inventário</td><td>Viewer</td></tr><tr><td><code>!deck</code></td><td>Ver suas cartas</td><td>Viewer</td></tr><tr><td><code>!mochila</code></td><td>Ver seus pacotes</td><td>Viewer</td></tr><tr><td><code>!pontos</code></td><td>Ver seus pontos</td><td>Viewer</td></tr><tr><td><code>!daily</code></td><td>Recompensa diária</td><td>Viewer</td></tr><tr><td><code>!carta &#x3C;nome></code></td><td>Ver info de uma carta</td><td>Viewer</td></tr><tr><td><code>!pacote &#x3C;nome></code></td><td>Ver info de um pacote</td><td>Viewer</td></tr><tr><td><code>!comprar &#x3C;nome></code></td><td>Comprar um item</td><td>Viewer</td></tr><tr><td><code>!vender &#x3C;nome></code></td><td>Vender um item</td><td>Viewer</td></tr><tr><td><code>!presentear @user &#x3C;nome></code></td><td>Presentear um usuário</td><td>Viewer</td></tr><tr><td><code>!troca @user &#x3C;item></code></td><td>Propor troca</td><td>Viewer</td></tr><tr><td><code>!trocaoferta &#x3C;aceitar/recusar></code></td><td>Responder troca</td><td>Viewer</td></tr><tr><td><code>!trocasim</code></td><td>Aceitar troca</td><td>Viewer</td></tr><tr><td><code>!trocanao</code></td><td>Recusar troca</td><td>Viewer</td></tr><tr><td><code>!sou_carta</code></td><td>Especifica que é uma carta para o bot em situação de desambiguação</td><td>Viewer</td></tr><tr><td><code>!sou_pacote</code></td><td>Especifica que é um pacote para o bot em situação de desambiguação</td><td>Viewer</td></tr><tr><td><code>!missao</code></td><td>Ver missões ativas</td><td>Viewer</td></tr><tr><td><code>!conquista</code></td><td>Ver conquistas ativas</td><td>Viewer</td></tr><tr><td><code>!album</code></td><td>Ver progresso do álbum</td><td>Viewer</td></tr><tr><td><code>!dica</code></td><td>Pedir dica sobre spawn</td><td>Viewer</td></tr><tr><td><code>!ping</code></td><td>Testar se o bot está online</td><td>Viewer</td></tr><tr><td><code>!ajuda</code></td><td>Informa todos os comandos do bot</td><td>Viewer</td></tr><tr><td><code>!addpontos @usuario &#x3C;qtd></code></td><td>Adiciona pontos a um usuário</td><td>Moderador</td></tr><tr><td><code>!rempontos @usuario &#x3C;qtd></code></td><td>Remove pontos de um usuário</td><td>Moderador</td></tr><tr><td><code>!bloquear @usuario</code></td><td>Bloqueia um usuário de interagir com o Baralhada</td><td>Moderador</td></tr><tr><td><code>!desbloquear @usuario</code></td><td>Desbloqueia um usuário</td><td>Moderador</td></tr><tr><td><code>!dar @usuario &#x3C;id_carta/pacote></code></td><td>Adiciona uma carta/pacote no inventário de um usuário</td><td>Moderador</td></tr><tr><td><code>!remover @usuario &#x3C;id_carta/pacote></code></td><td>Remove uma carta/pacote do inventário de um usuário</td><td>Moderador</td></tr><tr><td><code>!spawnpack &#x3C;id_pacote></code></td><td>Spawna um pacote no chat</td><td>Moderador</td></tr></tbody></table>

***

## Cooldowns e Permissões

Cada comando tem:

* **Cooldown Global:** tempo de espera após um uso, independente do usuário
* **Cooldown de Usuário:** tempo que o usuário deve esperar para usar novamente
* **Permissão mínima:** `viewer`, `sub`, `vip`, `mod` ou `streamer`

{% hint style="info" %}
Todos os parâmetros são configuráveis no **Painel Admin → Comandos**.
{% endhint %}

***

## Slugs e Nomes de Itens

Quando um comando pede um nome de item (como `!comprar Teste`), o bot tenta encontrar o item pelo nome ou pelo seu **slug** (identificador único). Se o slug corresponder a uma carta e a um pacote ao mesmo tempo, o bot pedirá desambiguação com `!sou_carta` ou `!sou_pacote`. Veja [Desambiguação de Itens](desambiguacao-de-itens.md).
