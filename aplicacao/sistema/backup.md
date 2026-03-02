# Backup

## Por que Fazer Backup?

Todos os dados do Baralhada Bot (cartas, pacotes, usuários, inventários, pontos) ficam armazenados em arquivos locais na sua máquina. **Não há backup automático na nuvem.** Em caso de falha no disco ou reinstalação acidental, os dados podem ser perdidos permanentemente sem um backup.

## Criando um Backup

{% stepper %}
{% step %}
### Vá ao painel de Backup

Acesse Painel → Backup.
{% endstep %}

{% step %}
### Criar backup

Clique em **Criar Backup Agora**.
{% endstep %}

{% step %}
### Arquivo gerado

Um arquivo `.zip` é gerado contendo todos os arquivos de banco de dados.
{% endstep %}

{% step %}
### Local do backup

O backup é salvo na pasta de dados do aplicativo e listado na tela.
{% endstep %}
{% endstepper %}

## Baixando Backups

Na lista de backups, clique no botão de download para salvar o arquivo `.zip` em um local de sua escolha (HD externo, Google Drive, etc.).

## Restaurando um Backup

{% hint style="danger" %}
⚠️ Restaurar um backup **substitui todos os dados atuais permanentemente**. Esta ação não pode ser desfeita.
{% endhint %}

{% stepper %}
{% step %}
### Abrir restauração

Clique em **Restaurar Backup**.
{% endstep %}

{% step %}
### Selecionar arquivo

Selecione o arquivo `.zip` de backup.
{% endstep %}

{% step %}
### Confirmar

Confirme a ação.
{% endstep %}

{% step %}
### Reinício automático

O aplicativo reinicia automaticamente com os dados restaurados.
{% endstep %}
{% endstepper %}

## Localização dos Dados

Os dados ficam em:

```
Windows: C:\Users\[SeuNome]\AppData\Roaming\baralhada-bot\
```

Você pode fazer backup manualmente copiando esta pasta inteira.

## Boas Práticas

| Situação                    | Recomendação                                   |
| --------------------------- | ---------------------------------------------- |
| Antes de atualizações       | Sempre faça backup antes                       |
| Uso regular da live         | Backup semanal                                 |
| Grandes eventos ou sorteios | Backup antes e depois                          |
| Mudanças no servidor        | Backup antes de alterar configurações críticas |

## Migração para Outro Computador

{% stepper %}
{% step %}
### Criar backup no computador atual

Crie um backup no computador atual.
{% endstep %}

{% step %}
### Instalar no novo computador

Instale o Baralhada Bot no novo computador.
{% endstep %}

{% step %}
### Restaurar no novo computador

Restaure o backup na tela de Backup.
{% endstep %}

{% step %}
### Reconfigurar credenciais

Configure as credenciais do Twitch novamente (não são salvas no backup por segurança).
{% endstep %}
{% endstepper %}
