# 🌐 Link Público

O **Link Público** é uma funcionalidade que permite que os espectadores da sua live acessem uma página web estilizada e luxuosa para interagir com o bot sem precisar spammar o chat da Twitch.&#x20;

Para que isso seja 100% seguro (e eles não tenham acesso ao seu painel interno de administrador), nós usamos uma ferramenta profissional da indústria chamada **Ngrok**.

O Ngrok funciona criando um "túnel" seguro, blindado e restrito entre o seu computador e a internet, usando um endereço permanente grátis oferecido por eles. **Os viewers jamais saberão o seu endereço de internet real (IP)**.

***

### Como Configurar seu Link Público Gratuito

O Ngrok exige uma conta rápida gratuita, mas em troca oferece excelentes benefícios: **sem tela de senha chata, HTTPS rápido para imagens e 1 domínio permanente de graça!** Siga os passos:

{% stepper %}
{% step %}
### &#x20;Criando a Conta no Ngrok

Acesse o site oficial: [https://dashboard.ngrok.com/signup](https://dashboard.ngrok.com/signup) e cadastre-se gratuitamente
{% endstep %}

{% step %}
### Pegando seu Token de Autenticação (Authtoken)

Procure no menu lateral esquerdo por **Identity & Access -> Authtokens** e crie o seu Token (Ou na página principal procure por "Your Authtoken" para utilizar o padrão).&#x20;

{% hint style="info" %}
&#x20;Ao criar o TOKEN será informado apenas uma vez, salve ele antes de fechar a tela de confirmação. Senão terá que criar novamente.
{% endhint %}
{% endstep %}

{% step %}
### Criando seu Domínio Fixo Gratuito

No menu da esquerda, clique em **UniverseGateway -> Domains** e crie seu novo domínio no botão _**New Domain**_
{% endstep %}

{% step %}
### Ligando o Túnel

No painel de **Link Público**, cole o Token e o domínio nos campos de configuração
{% endstep %}
{% endstepper %}
