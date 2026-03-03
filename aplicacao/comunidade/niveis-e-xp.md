# 📈 Níveis e XP

### 🆙 O que é o XP (Experiência)

O XP é a pontuação que define o **Nível** do espectador. Enquanto os pontos são gastos, o Nível é um marcador permanente de status e fidelidade na live.

### ⚙️ Ajustando a Curva de Nível



{% stepper %}
{% step %}
### Vá em Painel → Níveis

Acesse a área de balanceamento de RPG do bot.
{% endstep %}

{% step %}
### Configure o XP Base

Defina a dificuldade inicial:

<table><thead><tr><th width="150">Cálculo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>XP Necessário</strong></td><td>Quanto XP é necessário para sair do Nível 1.</td></tr><tr><td><strong>Multiplicador Daily</strong></td><td>Multiplicador de pontos quando utiliza o comando <code>!daily</code></td></tr><tr><td><strong>Fator Sorte</strong></td><td>Até onde o usuário pode progredir.</td></tr></tbody></table>
{% endstep %}

{% step %}
### Teste o Balanceamento

Simule quanto tempo um viewer médio levaria para chegar ao nível 10 com as configurações atuais.
{% endstep %}
{% endstepper %}

## 💰 Benefícios de Progressão

Além do prestígio, o nível do usuário impacta diretamente na economia e na sorte dentro da live. Cria um motivo real para o viewer querer "upar".

### 📈 Multiplicador do Daily

Quanto maior o nível, mais pontos o usuário recebe ao utilizar o comando `!daily`.

* **Progressão**: O sistema adiciona um bônus ao valor base do daily para cada nível conquistado.
* **Impacto**: Isso premia a fidelidade a longo prazo, permitindo que usuários veteranos acumulem pontos com mais facilidade.

### 🍀 Fator de Sorte

O nível do espectador atua como um modificador de sorte passivo para o sistema de colecionáveis.

* **Raridade**: Usuários de níveis mais altos possuem uma chance aumentada de encontrar cartas **Raras, Épicas e Lendárias** ao abrir pacotes ou participar de drops.
* **Vantagem**: Esse bônus incentiva os colecionadores a subirem de nível para completar suas coleções de forma mais eficiente.

### 🎁 Recompensas de Level Up

Ao atingir novos patamares, o sistema pode entregar prêmios automáticos para o espectador.

* **Prêmios**: É possível configurar o ganho de **pontos**, **cartas** ou **pacotes** ao subir de nível.
* **Incentivo**: Cria uma gratificação imediata a cada conquista de nível, mantendo o engajamento alto.

{% hint style="info" %}
Por padrão, o bot dá um pequeno bônus de sorte em aberturas de pacotes para usuários de nível mais alto.
{% endhint %}

{% hint style="success" %}
Tente criar nomes personalizados para os níveis (ex: Level 1-10: Novato, Level 11-20: Cavaleiro) para aumentar a imersão na sua temática.
{% endhint %}



