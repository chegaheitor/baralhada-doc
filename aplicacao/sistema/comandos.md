# Comandos

## Configurando Comandos

Em **Painel → Comandos** você pode customizar cada comando do bot:

| Campo                   | Descrição                                                     |
| ----------------------- | ------------------------------------------------------------- |
| **Trigger**             | Palavra que ativa o comando após `!` (ex: `claim` → `!claim`) |
| **Cooldown Global**     | Segundos de espera após qualquer uso do comando               |
| **Cooldown de Usuário** | Segundos que o usuário precisa esperar para usar novamente    |
| **Permissão Mínima**    | Nível mínimo para usar o comando                              |
| **Ativo**               | Ligar/desligar o comando                                      |

## Níveis de Permissão

| Nível      | Quem pode usar          |
| ---------- | ----------------------- |
| `viewer`   | Qualquer pessoa no chat |
| `sub`      | Assinantes e acima      |
| `vip`      | VIPs, mods e streamer   |
| `mod`      | Moderadores e streamer  |
| `streamer` | Apenas o streamer       |

## Editando Mensagens

Cada comando tem mensagens de resposta editáveis. Para editar:

{% stepper %}
{% step %}
### Passo

Na linha do comando, clique em um dos badges de mensagem.
{% endstep %}

{% step %}
### Passo

O texto atual será exibido.
{% endstep %}

{% step %}
### Passo

Edite e salve.
{% endstep %}
{% endstepper %}

### Variáveis Disponíveis nas Mensagens

| Variável      | Descrição                               |
| ------------- | --------------------------------------- |
| `{username}`  | Nome do usuário que usou o comando      |
| `{points}`    | Pontos do usuário                       |
| `{item_name}` | Nome do item em questão                 |
| `{quantity}`  | Quantidade                              |
| `{target}`    | Usuário alvo (em comandos como `!gift`) |
| `{cooldown}`  | Tempo restante de cooldown              |

{% hint style="info" %}
As variáveis disponíveis variam por mensagem. Passe o mouse sobre o badge da mensagem no painel para ver o texto atual.
{% endhint %}

## Exemplos de Mensagens Customizadas

{% code title="claim_success (padrão)" %}
```
```
{% endcode %}

{% code title="daily_cooldown (personalizado)" %}
```
```
{% endcode %}
