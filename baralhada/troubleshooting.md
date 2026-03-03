# Troubleshooting

Se algo não está funcionando como deveria, siga os passos abaixo para as situações mais comuns:

### 1. Bot não entra no Chat

* **Token OAuth Inválido:** Verifique se o seu token em **Configurações** começa com `oauth:`.
* **Nome do Canal:** O nome do canal deve ser exatamente o seu login da Twitch (ex: `meuchanal` e não `Meu Canal`).
* **Erro de Firewall:** Certifique-se de que o aplicativo Baralhada tem permissão para acessar a internet.

### 2. Overlay não aparece no OBS

* **Navegador Local:** No OBS, a fonte de navegador deve apontar para o arquivo `overlay.html` local no seu computador.
* **Cache do Navegador:** Se você mudou as configurações e não refletiu no OBS, clique com o botão direito na fonte de navegador no OBS e selecione "Atualizar cache da página atual".
* **Status do Servidor:** O bot precisa estar aberto e rodando para o overlay funcionar, pois o overlay se comunica com o servidor local do bot (geralmente porta 3001).

### 3. Imagens de Cartas quebradas

* **Caminho do Arquivo:** Verifique se você não moveu as imagens da pasta original após cadastrá-las.
* **Formato Suportado:** Use apenas PNG, JPG ou GIF.

### 4. Erros de Banco de Dados

Se o bot exibir erros de "Database Locked" ou não salvar configurações:

* **Reinicie o App:** Feche o Baralhada completamente e abra-o novamente.
* **Permissões de Pasta:** Certifique-se de que a pasta `Documentos/Baralhada` não está marcada como "Somente Leitura".
