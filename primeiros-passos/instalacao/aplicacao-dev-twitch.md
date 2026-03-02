# Aplicação Dev Twitch

## 🔑 Como obter seu Client ID e Client Secret (Helix API)

Para que o bot possa acessar funcionalidades avançadas da Twitch (como buscar informações de usuários, perfis e validar lives), você precisa criar uma "Aplicação" no portal de desenvolvedores da Twitch.

Siga os passos abaixo:

### 1. Acesse o Console de Desenvolvedores

Vá para [Twitch Dev Console](https://dev.twitch.tv/console/apps) e faça login com sua conta da Twitch.

### 2. Registre sua Aplicação

1. Clique no botão **"+ Registre o seu aplicativo"**.
2. **Name:** Escolha um nome para sua aplicação (ex: `MeuBotDeCartas`).
3. **URLs de redirecionamento OAuth:** Digite `http://localhost`. (Não se preocupe, não usaremos isso agora, mas é obrigatório). Clique em **Add**.
4. **Categoria:** Selecione **Chat Bot** ou **Other**.
5. **Tipo de Cliente:** Deixe como **Confidencial** (se aparecer).
6. Resolva o CAPTCHA e clique em **Criar**.

### 3. Pegue suas Credenciais

1. Na lista de aplicações, clique em **Gerenciar** na aplicação que você acabou de criar.
2. Você verá o campo **ID do Cliente**. Copie este código.
3.  Logo abaixo, clique no botão **"Novo Segredo"**.

    > \[!WARNING] O **Client Secret** só aparece UMA VEZ. Copie-o e guarde em um lugar seguro imediatamente! Se você sair da página sem copiar, terá que gerar um novo.

### 4. Configure no Baralhada Bot

Agora, abra o painel administrativo do seu bot:

1. Vá em **Configurações** > **Twitch e Conexão**.
2. Cole o **Client ID** e o **Client Secret** nos campos correspondentes.
3. Salve as configurações.
