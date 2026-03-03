# Backup

## 💾 O que é o Sistema de Backup

O sistema gera arquivos compactados contendo todo o seu banco de dados (cartas, usuários, saldos e logs). Em caso de mudança de computador ou erro grave, você pode restaurar tudo em segundos.

### 🛠️ Gerando e Restaurando um Backup

{% stepper %}
{% step %}
### Vá em Painel → Backup

Aqui você encontra a lista de backups manuais e automáticos.
{% endstep %}

{% step %}
### Clique em Criar Backup

O sistema processará os dados e gerará um arquivo `.json` ou `.zip` para download.
{% endstep %}

{% step %}
### Salve Externamente

Não deixe o backup apenas no mesmo computador. Salve na nuvem para ter certeza que não irá perder
{% endstep %}

{% step %}
### Restaurar (Se necessário)

Arraste o arquivo de backup para a área de restauração para sobrepor os dados atuais.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Antes de deletar uma coleção inteira, crie um backup manual!
{% endhint %}

## ⁉ Por que Fazer Backup?

Todos os dados do Baralhada Bot (cartas, pacotes, usuários, inventários, pontos) ficam armazenados em arquivos locais na sua máquina. **Não há backup automático na nuvem, nem conexão com internet.** Em caso de falha no disco ou reinstalação acidental, os dados podem ser perdidos permanentemente sem um backup.

### 🛡️ Prevenção de Perdas

* **Impacto**: Garante a continuidade do seu "card game" por anos, independente de falhas de hardware.
* **Dica**: Faça um backup semanal se sua live for muito ativa (com muitas trocas e spawns).

{% hint style="danger" %}
**Atenção:** Restaurar um backup antigo irá APAGAR qualquer progresso feito entre a data do backup e hoje. Use com cautela extrema.
{% endhint %}

## Restaurando um Backup

{% stepper %}
{% step %}
### Vá em Painel → Backup

Selecione o tipo de opção de backup que você de restaurar.
{% endstep %}

{% step %}
### Selecionar arquivo

Selecione o arquivo `.zip` / `.db` de backup.
{% endstep %}

{% step %}
### Confirmar

Confirme a ação.
{% endstep %}
{% endstepper %}

## 📁 Localização dos Dados

Por padrão, todos os arquivos de banco de dados (`.db`) e backups são armazenados em sua pasta de documentos do Windows:

```
Meus Documentos > Baralhada > database
```

Você pode fazer backup manualmente copiando esta pasta inteira.

## 🛠️ Categorias de Dados

O sistema organiza os backups em grupos lógicos para facilitar a gestão:

| Categoria                 | Descrição                                      | Principais Arquivos                                 |
| ------------------------- | ---------------------------------------------- | --------------------------------------------------- |
| **🌍 Global & Essencial** | Backup Geral (ZIP) e Configurações base.       | `FULL_backup.zip`, `settings.db`                    |
| **👥 Jogadores & Perfis** | Dados básicos, pontos, níveis e XP acumulado.  | `users.db`                                          |
| **🎴 Catálogo de Cartas** | Definições de Cartas, Pacotes e Raridades.     | `cards.db`, `packs.db`, `card_rarities.db`          |
| **🎒 Inventário**         | O que cada usuário possui (Mochila e Cartas).  | `user_cards.db`, `user_packs.db`                    |
| **📈 Progresso**          | Status de Missões e Conquistas dos jogadores.  | `user_missions.db`, `user_achievements.db`          |
| **📜 Eventos & Logs**     | Histórico de Spawns e registros de atividades. | `spawns.db`, `activity.db`                          |
| **⚙️ Personalização**     | Comandos Custom, Mensagens do Bot e Alertas.   | `commands.db`, `messages.db`, `overlay_settings.db` |

{% hint style="warning" %}
O **Backup GERAL** é a forma mais segura de migrar o bot entre diferentes computadores ou fazer uma cópia de segurança completa antes de grandes atualizações.
{% endhint %}

## 🧹 Limpeza de Dados (Reset)

No painel administrativo, cada categoria possui um botão **Limpar**.

* **O que faz?** Apaga todos os registros daquela categoria específica (ex: dar um "wipe" apenas nas cartas dos usuários para começar uma nova temporada).
* **Segurança:** Esta ação é **irreversível**. O sistema solicitará confirmações múltiplas antes de apagar o arquivo físico.

## ⚡ Otimização do Banco (Faxina)

O botão **Otimizar Banco (Faxina)** no cabeçalho da página é uma das ferramentas mais importantes de manutenção.

#### ❓ Por que otimizar?

O bot utiliza o banco de dados NeDB, que trabalha com um sistema de **Append-Only**. Isso significa que, para ser mais rápido na escrita, ele não apaga os dados antigos quando você os edita; ele apenas escreve a versão nova no final do arquivo. Com o tempo, o arquivo `.db` fica cheio de versões obsoletas dos mesmos dados, aumentando o tamanho do arquivo desnecessariamente.

#### ✨ O que a Faxina realiza:

1. **Compactação:** Lê o arquivo inteiro e reescreve apenas a versão mais atual de cada registro.
2. **Performance:** Reduz drasticamente o tamanho do arquivo e acelera o tempo de resposta do bot.
3. **Relatório:** Ao final, o sistema mostra exatamente quantas entradas foram removidas de cada banco.

<details>

<summary>🚀 <strong>O processo de faxina pesa no desempenho?</strong></summary>

Não, ele faz o oposto. Como o bot utiliza o sistema **Append-Only** (onde novas informações são apenas empilhadas no final do arquivo), o banco pode crescer desnecessariamente. A faxina "enxuga" o arquivo, tornando as leituras e gravações mais rápidas.

</details>

<details>

<summary>🔍 <strong>Como ele sabe qual é a versão correta dos dados?</strong></summary>

O sistema identifica o registro mais recente (o último a ser gravado) para cada ID único. Durante a faxina, ele descarta as versões obsoletas e reescreve apenas o dado mais atual no arquivo físico.

</details>

<details>

<summary>🖱️ <strong>Preciso fazer faxina manualmente?</strong></summary>

Não é obrigatório. O **Baralhada Bot** realiza uma faxina automática em todos os arquivos `.db` a cada **1 hora aberto**. O botão manual é útil principalmente após realizar grandes limpezas ou resetar categorias específicas.

</details>

<details>

<summary>🛡️ <strong>Isso pode apagar meus dados?</strong></summary>

**De forma alguma.** A faxina remove apenas o histórico de alterações antigas de um mesmo registro. Seus dados atuais, inventários e progresso dos jogadores permanecem 100% seguros.

</details>

