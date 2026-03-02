# Instalação

## 💻 Requisitos

| Plataforma                                      | Requisitos                                                           |
| ----------------------------------------------- | -------------------------------------------------------------------- |
| Windows                                         | 10 ou superior                                                       |
| Conta Principal (Streamer)                      | Conta principal aonde os viewers podem utilizar da aplicação         |
| Conta Secundária (Bot)                          | Conta do bot que mandará mensagens e fará conexão com a aplicação    |
| [Oauth Token Bot](oauth-token-bot.md)           | Token de autentição do bot para ele funcionar e interagir com o chat |
| [Aplicação Dev Twitch](aplicacao-dev-twitch.md) | Client ID e Client Secret (para detectar as fotos dos viewers)       |

{% hint style="info" %}
Dica: Crie uma conta Twitch separada para o bot, como `NomeDaLiveBot` ou `NomeDaLiveTCG`.
{% endhint %}

***

## 🛠 Instalação&#x20;

{% stepper %}
{% step %}
### Baixar o instalador

Baixe o arquivo `Baralhada.exe` na página de downloads.
{% endstep %}

{% step %}
### Executar o instalador

Execute o instalador e siga as instruções.
{% endstep %}

{% step %}
### Atalho

O programa será instalado e um atalho criado no Desktop.
{% endstep %}

{% step %}
### Abrir o aplicativo

Abra o **Baralhada Bot** pelo atalho.
{% endstep %}
{% endstepper %}

***

## 📊 Dados e Banco de Dados

Os dados são salvdoasd sadutomaticamente em:

```
Windows: C:\Users\SeuNome\Documents\Baralhada
Pasta Baralhada em Meus Documentos 
```

Esta pasta contém os arquivos `.db` com todos os dados (cartas, usuários, inventários, etc.).

{% hint style="warning" %}
Recomendamos que faça backup desta pasta regularmente.
{% endhint %}
