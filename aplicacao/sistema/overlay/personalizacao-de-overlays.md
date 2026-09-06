# 🎨 Personalização de Overlays

Este documento foi criado para streamers, desenvolvedores e criadores de conteúdo que desejam personalizar a identidade visual dos alertas de tela (Browser Source do OBS Studio) do **Baralhada**.

***

## 🖥️ Visão Geral

O Baralhada possui um sistema de alertas visuais transmitidos em tempo real para a sua stream através de uma **Fonte de Navegador (Browser Source)** no OBS Studio (`http://localhost:PORTA/#/overlay`).

Por padrão, o sistema renderiza componentes com design neo-brutalista moderno. No entanto, se você souber **HTML, CSS e JavaScript**, você tem total liberdade para criar layouts 100% personalizados para cada tipo de evento do jogo.

***

## 🎨 Como acessar o editor de personalização

1. No menu lateral do programa, clique em **Configurações de Overlay** (`/overlay-settings`).
2. Localize o card do tipo de overlay que deseja modificar (ex: _Spawn de Pacote_, _Abertura de Pacote_, _Duelo_, etc.).
3. Clique no botão **"Personalizar"** (ícone de código `</>`).
4. A janela de personalização será aberta com:
   * **Editor de Código**: Área onde você digita ou cola seu HTML/CSS/JS.
   * **Variáveis Disponíveis**: Painel lateral listando todas as variáveis daquele evento (clique em qualquer variável para copiá-la).
   * **Botão "Carregar Padrão no Editor"**: Carrega o código padrão oficial para você começar a editar sem precisar escrever tudo do zero.
   * **Botão "Restaurar Padrão do Sistema"**: Remove suas alterações e volta o overlay para o layout nativo do sistema.
   * **Botão "Testar no OBS"**: Dispara o evento de teste instantaneamente para você validar o visual no OBS ou no navegador.
   * **Botão "Salvar Personalização"**: Aplica as alterações imediatamente na sua live.

***

## ⌨️ Programar um overlay

Você pode escrever uma página completa com `<style>`, tags HTML e `<script>`. O código é executado de forma isolada e segura, mantendo o fundo transparente.

#### Usando Placeholders no HTML

Qualquer variável do evento pode ser interpolada diretamente no seu HTML usando chaves duplas:

```html
<h1>{{data.packName}}</h1>
<img src="{{data.image}}" alt="{{data.packName}}" />
<p>Resgate digitando: {{data.triggers.claim}}</p>
```

#### Usando JavaScript Nativo (`window.overlayData`)

Para eventos com listas de dados (como as cartas tiradas em um pacote) ou lógica avançada (sons, timers, loops), o sistema disponibiliza o objeto global:

```javascript
window.overlayData
```

Exemplo:

```html
<div id="minhas-cartas"></div>

<script>
  const evento = window.overlayData || {};
  const cartas = evento.data?.cards || [];

  cartas.forEach(carta => {
    console.log("Carta:", carta.name, carta.rarity);
  });
</script>
```

## 🔄️ Restaurar para o Padrão

Se em algum momento você quiser descartar sua personalização e voltar ao design nativo do sistema:

1. Acesse **Configurações de Overlay** no programa.
2. Clique no botão **"Personalizar"** do overlay desejado.
3. No cabeçalho da janela, clique em **"Restaurar Padrão do Sistema"** (em vermelho).
4. Confirme a operação. O código personalizado será deletado e o overlay voltará imediatamente para o design original em React.

{% hint style="info" %}
Essa operação é irreversível, lembre-se de usar com cuidado.
{% endhint %}

***

## 💡 Dicas e Efeitos Avançados

#### 🎵 Como Tocar um Efeito Sonoro Customizado

Você pode tocar arquivos de áudio locais (da pasta de uploads ou da web) via `<script>`:

```html
<script>
  // Toca um som quando o overlay surgir
  const audio = new Audio('/uploads/meu_som_especial.mp3');
  audio.volume = 0.6;
  audio.play().catch(e => console.log('Áudio aguardando interação'));
</script>
```

#### 🎨 Importar Fontes Customizadas

Utilize `@import` no topo da sua tag `<style>`:

```css
@import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@700&display=swap');

body {
  font-family: 'Cinzel', serif;
}
```

#### 💫 Animações com Keyframes

Para criar alertas que deslizam da esquerda ou giram:

```css
@keyframes entrarSuave {
  from {
    opacity: 0;
    transform: translateY(50px) scale(0.9);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

.meu-alerta {
  animation: entrarSuave 0.4s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}
```

Pronto! Agora você tem controle total para deixar os overlays da sua transmissão com a cara do seu canal!
