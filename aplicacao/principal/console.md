# Console

## 🖥️ Para que serve o Console?

O Console exibe as mensagens internas do bot. Se algo não está funcionando (o bot não responde no chat, a Twitch desconectou, o arquivo de áudio não tocou), a resposta estará aqui.

### 🛠️ Funcionalidades de Monitoramento

#### 🚥 Tipos de Mensagens (Cores)

* **🟦 INFO:** Batidas de coração do sistema, confirmando que processos estão rodando.
* **🟩 SUCCESS:** Ações concluídas com êxito (ex: Bot conectado com sucesso!).
* **🟧 WARN:** Alertas que não param o bot, mas merecem atenção (ex: Tentativa de comando inválido).
* **🟥 ERROR:** Problemas críticos (ex: Falha de autenticação com a Twitch ou banco corrompido).

#### 🏷️ Categorias de Filtragem

Você pode filtrar o console por área de interesse:

* **SYSTEM:** Inicialização e processos do Windows/Electron.
* **ADMIN:** Ações de administrações.
* **BOT:** Lógica das cartas e processamento de comandos.
* **TWITCH:** Conexão, Chat e eventos da API Helix.
* **DATABASE:** Operações de leitura/escrita nos arquivos `.db`.

## ⌨️ Controles do Console

* **⏸️ Pausar Rolagem:** Útil quando muitos erros estão acontecendo e você precisa ler uma linha específica sem que ela "fuja" para cima.
* **🔍 Busca em Tempo Real:** Filtre as mensagens que contêm palavras específicas.
* **🗑️ Limpar Console:** Limpa a visualização atual para facilitar o início de um novo teste.

### 🛡️ Dica de Ouro: "O Inspecionador JSON"

Muitas mensagens do console possuem o botão **JSON** ao lado. Clique nele para ver os dados brutos que o bot recebeu da Twitch ou do Banco. Isso é fundamental para programadores e usuários avançados que querem entender exatamente o que está acontecendo por trás das cortinas.

{% hint style="success" %}
**Status do Socket:** No rodapé do console, existe um indicador de estabilidade. Se ele estiver verde e piscando, a comunicação entre o bot e o painel administrativo está perfeita!
{% endhint %}

{% hint style="danger" %}
**Aviso:** Erros vermelhos constantes no console indicam que algo precisa ser corrigido imediatamente. Geralmente são credenciais de API (`Client ID`) configuradas incorretamente.
{% endhint %}

