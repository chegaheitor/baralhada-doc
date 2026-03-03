# ⌨️ Comandos

## ⌨️ O que é o Gerenciador de Comandos

O bot vem com comandos padrão (ex: `!deck`), mas nesta página você pode renomear o comando para o que desejar (ex: `!cartas`) e definir quem tem permissão para usá-lo.

### 🛠️ Personalizando um Comando

{% stepper %}
{% step %}
### Vá em Painel → Comandos

Veja a lista de todos os comandos ativos e inativos do sistema.
{% endstep %}

{% step %}
### Escolha o Comando

Clique no comando que deseja editar para abrir as configurações de gatilho e permissão.
{% endstep %}

{% step %}
### Preencha as Configurações

Ajuste os campos conforme sua necessidade:

<table><thead><tr><th width="150">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Gatilho Principal</strong></td><td>A palavra que dispara o comando (ex: <code>!perfil</code>).</td></tr><tr><td><strong>Cargo Mínimo</strong></td><td>Nível de permissão (Viewer, Sub, VIP, Mod, Streamer).</td></tr><tr><td><strong>Cooldown Usuário e Global</strong></td><td>Tempo de espera entre usos para evitar spam (em segundos).</td></tr><tr><td><strong>Ativo</strong></td><td>Habilitar ou desabilitar o comando completamente.</td></tr></tbody></table>
{% endstep %}
{% endstepper %}

{% hint style="info" %}
SEMPRE configure um cooldown (ex: 5-10 segundos) para comandos de consulta frequente. Evita spam na sua live.
{% endhint %}

## 🔐 Hierarquia de Permissões

Define quem pode "mandar" no bot. Permissões é de extrema importância.

* **Impacto**: Impede que espectadores comuns usem comandos administrativos como `!dar` ou `!addpontos`.

### 🕒 Cooldown Global vs Usuário

* **Usuário**: O viewer X precisa esperar para usar o comando de novo.
* **Global:** Todos os viewers precisam esperar para usar o comando novamente.
* **Impacto**: Essencial para manter a leitura do chat fluida e o bot sempre responsivo.

{% hint style="success" %}
**Dica Pro:** Renomeie os comandos para o tema da sua live! Se você joga um RPG medieval, mude `!deck` para `!grimorio`.
{% endhint %}

## 📶 Níveis de Permissão

<table><thead><tr><th width="284">Nível</th><th>Quem pode usar</th></tr></thead><tbody><tr><td><code>streamer</code></td><td>Apenas o streamer</td></tr><tr><td><code>mod</code></td><td>Moderadores e streamer</td></tr><tr><td><code>vip</code></td><td>VIPs, mods e streamer</td></tr><tr><td><code>sub</code></td><td>Assinantes e acima</td></tr><tr><td><code>viewer</code></td><td>Qualquer pessoa no chat</td></tr></tbody></table>

## ⚡ Atualização em Tempo Real

As alterações nos comandos são aplicadas em tempo real. Assim que você salvar as modificações no painel, o bot passará a usar as novas configurações imediatamente, sem a necessidade de reiniciar o programa ou o bot.

<details>

<summary>⚙ <strong>É possível criar meus próprios comandos?</strong></summary>

Ainda no momento não é possível utilizar o Baralhada para criar seus próprios comandos, como um bot de twitch (exemplo: streamelements, streamlabs).&#x20;

</details>
