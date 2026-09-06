# 🖼️ Overlay

## 📺 O que é o Overlay

É uma página web transparente que você adiciona ao seu OBS/Streamlabs. Quando o bot executa uma ação (como um Spawn ou Pack Opening), o Overlay exibe animações e artes em tempo real. Transforme seu OBS em uma experiência interativa. O Overlay é onde a mágica acontece visualmente para quem assiste.

### 🛠️ Configurando seu Overlay

{% stepper %}
{% step %}
### Vá em **Painel → Overlay**

Você pode usar a **URL Online** (mais simples) ou o **Arquivo Local** (mais performance).
{% endstep %}

{% step %}
### Adicione ao OBS

Crie uma nova fonte de **Navegador (Browser Source)**:

* **URL**: Cole o link copiado.
* **Largura/Altura**: 1920x1080 (ou a resolução da sua base).
* **Transparência**: Certifique-se de que o fundo esteja transparente.
{% endstep %}

{% step %}
### Teste o Visual

Use os botões de "Teste" no painel para ver as animações sem precisar esperar um spawn real.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Aceleração de Hardware: Ative esta opção no OBS para animações mais fluidas.
{% endhint %}

## 📋 Tipos de Overlays Disponíveis

O bot possui diversos alertas independentes que você pode ativar, desativar e testar:

| Alerta          | O que exibe?                                 | Teste Manual |
| --------------- | -------------------------------------------- | ------------ |
| **📦 Spawn**    | Quando um pacote "selvagem" surge no chat.   | Sim          |
| **✨ Abertura**  | As cartas saindo do pacote após o `!abrir`.  | Sim          |
| **🔍 Inspeção** | Detalhes de uma carta ou pacote específico.  | Sim          |
| **📖 Álbum**    | O progresso de coleção de um usuário.        | Sim          |
| **🤝 Troca**    | Celebração visual de uma troca bem-sucedida. | Sim          |
| **🎁 Presente** | Animação de envio/recebimento de presente.   | Sim          |
|                 |                                              |              |

## 🏠 Overlay Local (Arquivo HTML)

Pensando em quem tem internet instável ou quer o máximo de performance, o bot permite exportar o overlay.

* **Como gerar:** No painel de Overlays, clique em **"Gerar arquivo HTML para o OBS"**.
* **Onde fica:** O arquivo será criado em `📁 Documentos > Baralhada > overlay.html`.
* **Vantagem:** O OBS carrega os arquivos direto do seu disco, evitando atrasos de rede na hora de exibir as animações.

{% hint style="success" %}
**Dica de Ouro:** Posicione o Overlay em uma camada no topo de tudo, para que as cartas "pulem" na frente de tudo quando alguém ganhar!
{% endhint %}

## 👤 Fotos de Usuários

Alguns overlays utilizam as fotos de perfil dos usuários da Twitch (como em **Trocas**, **Presentes** e **Abertura de Pacotes**) para tornar a experiência mais visual e personalizada. O administrador pode ativar ou desativar a exibição dessas imagens globalmente nas configurações do painel.

## ⚙️ Configurações dos Alertas

Cada tipo de overlay possui ajustes individuais para melhor se adaptar à sua live:

* **Tempo de Exibição:** Defina exatamente por quantos segundos cada animação deve permanecer visível antes de desaparecer.
* **Ativar/Desativar:** Você tem total controle para escolher quais alertas deseja que apareçam na tela e quais prefere manter ocultos.
