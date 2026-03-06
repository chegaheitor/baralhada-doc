# 💾 Desempenho

## 📊 O que é o Monitor de Sistema

O **Monitor de Sistema** é uma ferramenta de telemetria em tempo real integrada ao painel administrativo. Ele permite que você acompanhe a "saúde" técnica do seu bot e do servidor onde ele está hospedado, garantindo que a live corra sem travamentos.

### 📈 Métricas Monitoradas

O painel exibe quatro cards principais de telemetria:

#### ⚡ CPU (Processamento)

Mostra a carga atual de trabalho do processador do servidor.

* **Uso (%)**: Percentual de processamento sendo utilizado no momento.
* **Cores**: Quantidade de núcleos detectados.
* **Modelo**: Identificação técnica do processador.

#### 🧠 RAM Sistema (Memória Total)

Monitora quanto da memória RAM total do servidor está em uso por todos os processos ativos.

* **Gráfico de Barra**: Visualização rápida da ocupação da memória.
* **Valores**: Exibe o uso em GB/MB (ex: 2.5 GB / 8 GB).

#### 🚀 Memória do Processo (App Memory)

Esta é a métrica mais importante para o bot. Ela mostra quanto de memória RAM **apenas o bot** está consumindo (**RSS**).

* Ajuda a identificar se o bot está ficando "pesado" devido a muitos usuários ou comandos simultâneos.

#### ⏰ Uptime (Tempo de Atividade)

Cronômetro que mostra há quanto tempo o bot está online e operante sem reinicializações.

***

### 📉 Gráficos de Histórico

O monitor mantém um histórico visual dos últimos minutos:

* **Histórico de CPU**: Área chart que mostra as oscilações de processamento.
* **Alocação de Memória**: Acompanha a curva de consumo de RAM do processo do bot.

***

### 🛠️ Especificações Técnicas

No rodapé da página, você encontra dados fixos do ambiente:

* **Plataforma**: Sistema operacional (ex: win32) e arquitetura (ex: x64).
* **Status do Servidor**: Indicador visual de estabilidade.
* **Última Atualização**: Carimbo de tempo da última coleta de dados (o monitor atualiza a cada 3 segundos).

{% hint style="info" %}
**Quando verificar?** Se o chat da Twitch parecer lento para responder aos comandos, dê uma olhada no Monitor. Se o uso de CPU estiver perto de 100%, pode ser necessário fechar outros programas no computador onde o bot está rodando.
{% endhint %}
