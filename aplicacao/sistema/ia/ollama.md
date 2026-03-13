# 🦙 Ollama

O Ollama é a sua ponte para usar modelos de linguagem de Inteligência Artificial pesados rodando **100% no seu próprio computador**. A principal vantagem? **É totalmente de graça, rápido e privado.** Sem limites mensais de API ou bloqueios.

## 🚀 Passo a Passo de Instalação Básica

### 🤖 Obtendo o Motor (Ollama)

1. Acesse [ollama.com](https://ollama.com) e baixe a versão para o seu sistema operacional (Windows/Mac/Linux).
2. Siga o instalador padrão ("Next, Next, Finish").
3. Após instalado, um pequeno ícone em formato de Lhama aparecerá na sua bandeja do sistema (perto do relógio do Windows). Isso significa que o servidor está pronto.

### 🧠´Escolhendo e Baixando o Seu "Cérebro"

O Ollama é o motor, mas ele precisa de um "modelo" (o cérebro) para pensar. Recomendamos a versão super rápida e leve da Meta, o Llama 3.2.

1. Abra o seu Terminal (Prompt de Comando ou PowerShell).
2.  Digite o comando abaixo e aperte Enter:

    ```bash
    ollama run llama3.2:1b
    ```
3. Ele começará a baixar um arquivo grande (1 a 2GB). Aguarde terminar.
4. Quando aparecer a palavra `>>> Send a message (/? for help)` e piscar um cursor no terminal, quer dizer que o cérebro baixou e ligou!
5. Teste dando um "Oi!" pelo terminal, se ele responder em português... Sucesso.
6. Você pode **fechar o terminal**. O ícone do Ollama na bandeja do Windows garante que ele continua funcionando no fundo preparado para o Bot de Cartas.

### 🔗 Conectando no Baralhada Bot

1. No seu Painel de Controle (Dashboard do Bot), vá em **Sistema > IA**.
2. Ative a chave **IA Ativada**.
3. Selecione o provedor **Ollama (Local)**.
4. No campo **Ollama URL**, não mude, mantenha: [`http://127.0.0.1:11434`](http://127.0.0.1:11434)
5. No campo **Modelo (Ex: llama3.2:1b)**, digite ESPECIFICAMENTE o modelo que você acabou de baixar no Passo 2. Exemplos: `llama3.2:1b` ou `mistral`.
6. Salve e clique em **Testar**. Ele deverá te retornar uma saudação robótica no painel vermelho.

***

### 🧠 Modelos Recomendados e Hardware

<table><thead><tr><th width="148">Modelo</th><th>Recomendação do Dev</th><th width="185">Peso na Memória (RAM/VRAM)</th><th>Descrição e Personalidade</th></tr></thead><tbody><tr><td><strong><code>llama3.2:1b</code></strong></td><td>🥇 <strong>A Melhor Escolha!</strong></td><td><em>Ultra Leve (~1.5 GB)</em></td><td>Perfeito, sarcástico e estupidamente rápido de carregar e escrever até em PCs sem placa de vídeo (GPU) gamer. Equilíbrio de inteligência perfeito para as fofocas.</td></tr><tr><td><strong><code>gemma:2b</code></strong></td><td>🥈 Alternativa (Google)</td><td><em>Leve (~2 GB)</em></td><td>Muito bom em português, ideal se o Llama 3 não estiver no estilo que você busca em suas respostas do Bot.</td></tr><tr><td><strong><code>mistral</code></strong></td><td>🥉 Pós-Graduados</td><td><em>Pesado (~5 a 8 GB)</em></td><td>Extremamente detalhista, maduro. Se o seu Prompt pedir textos longos, é perfeito. Atrasará na transmissão e exigirá um PC com hardware monstro atual.</td></tr></tbody></table>

**Como instalo outro modelo para testar?** Basta abrir seu CMD/Terminal, digitar `ollama run nomedomodelo` e, depois de carregar, trocar o texto do modelo no painel do bot.

## ⚠️ Solução de Problemas Comuns

1. **"Falha ao conectar.../Timeout":**
   * Verifique se o ícone da lhama do Ollama está do lado do relógio do relógio do Windows, caso não, abra o aplicativo Ollama pelo menu Iniciar.
   * Se o bot acusar "timeout of 30000ms", ou o seu PC está muito sobrecarregado jogando + rodando IA local, ou o seu modelo escolhido (`mistral` por exemplo) é pesado demais para sua máquina, demorando mais de 30 segundos para pensar em uma única palavra. Considere trocar para o `llama3.2:1b`.
2. **"Ollama Error: model '...' not found":**
   * Você digitou o nome no painel ERRADO. Você precisa digitar o formato idêntico ao que usou para baixar: `llama3.2:1b`.
3. **Demora Enorme para Responder (Bot Lento):**
   * Troque para um modelo mais fraco que termine com `:1b` (One Billion Parameters).
   * Lembre-se que streaming usa MUITA CPU/Placa de vídeo pela OBS! Sobra menos poder livre do seu computador para o cérebro do Ollama funcionar rápido.
