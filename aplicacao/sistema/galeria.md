# 🖼️ Galeria

A **Galeria de Uploads** é uma funcionalidade integrada ao **Baralhada** que permite visualizar, auditar, buscar, filtrar e organizar todos os arquivos de mídia (imagens de cartas, capas de pacotes, áudios e outros uploads) em um único painel centralizado.

Além de fornecer uma interface visual moderna e rápida, o sistema conta com uma estrutura de diretórios categorizada e mecanismos inteligentes de **migração automática** e **retrocompatibilidade**, garantindo que seus overlays e banco de dados continuem funcionando perfeitamente sem links quebrados.

***

### 🚀 O que é a Galeria de Uploads?

Com a Galeria de Uploads:

* Todos os arquivos são organizados automaticamente em subpastas categorizadas (`cards/`, `packs/`, `sounds/`, `others/`).
* Você pode visualizar miniaturas em alta qualidade de todas as mídias salvas no bot.
* Efeitos sonoros contam com um player de áudio integrado na própria interface.
* O sistema possui um botão para abrir a pasta diretamente no Windows Explorer.
* Métricas em tempo real mostram o número total de arquivos e a quantidade de espaço em disco utilizada.

***

### 📁 Estrutura de Pastas no Disco

Todos os uploads ficam localizados no seu diretório de dados do usuário: `~/Documents/Baralhada/uploads/` (ou `<pasta_do_bot>/uploads/`).

Dentro desta pasta, o sistema organiza os arquivos em 4 categorias oficiais:

| Subpasta  | Categoria                      | Tipos de Arquivos Suportados                     |
| --------- | ------------------------------ | ------------------------------------------------ |
| `cards/`  | 🃏 Imagens de Cartas           | `.png`, `.jpg`, `.jpeg`, `.webp`, `.gif`, `.svg` |
| `packs/`  | 📦 Capas de Pacotes/Boosters   | `.png`, `.jpg`, `.jpeg`, `.webp`, `.gif`         |
| `sounds/` | 🔊 Efeitos Sonoros e Áudios    | `.mp3`, `.wav`, `.ogg`, `.m4a`, `.aac`           |
| `others/` | 📁 Conquistas, Ícones e Outros | Outros formatos de imagem e arquivos gerais      |

#### 🔄 Auto-Organização e Migração Inteligente

Ao iniciar o Baralhada, o servidor executa uma rotina em segundo plano que:

* Identifica arquivos que ainda estejam soltos na raiz de `uploads/`.
* Consulta o banco de dados (`cards.db` e `packs.db`) para associar cada imagem ao seu respectivo item.
* Move os arquivos para `uploads/cards/` ou `uploads/packs/` de forma segura.
* Atualiza as URLs salvas no banco de dados e limpa referências antigas.

***

### 📱 Recursos da Interface da Galeria

| Recurso                                    | Descrição                                                                                                                                                 |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **📊 Painel de Métricas**                  | Mostra o total de arquivos armazenados, o espaço total consumido em disco e a contagem específica de cada categoria.                                      |
| **🏷️ Abas de Categorias**                 | Permite alternar rapidamente entre **Todas**, **🃏 Cartas**, **📦 Pacotes**, **🔊 Sons** e **📁 Outros**, exibindo a quantidade de itens em cada aba.     |
| **🔍 Busca em Tempo Real**                 | Campo de busca instantânea pelo nome do arquivo (ex: buscar "dragao" filtra imediatamente todas as mídias correspondentes).                               |
| **🎛️ Filtro de Extensões**                | Filtre apenas por formatos específicos como `.png`, `.jpg`, `.webp`, `.gif`, `.mp3`, `.wav`, etc.                                                         |
| **🎵 Player de Áudio Integrado**           | Permite ouvir efeitos sonoros diretamente pela galeria com barra de progresso, botão play/pause e controle de volume sem precisar abrir players externos. |
| **🔎 Modal de Detalhes em Alta Resolução** | Clique em qualquer imagem para inspecioná-la ampliada, conferir dimensões em pixels, tamanho exato em KB/MB, data de modificação e link direto.           |
| **📋 Copiar URL Direta**                   | Botão para copiar o link interno do arquivo (ex: `/uploads/cards/exemplo.png`) para colar facilmente em overlays ou configurações.                        |
| **🗑️ Exclusão Segura**                    | Permite deletar arquivos desnecessários do disco com modal de confirmação para prevenir cliques acidentais.                                               |
| **📂 Botão "Abrir Pasta"**                 | Abre a pasta de uploads diretamente no Windows Explorer do seu computador com apenas um clique.                                                           |
| **🖼️ Seletor nos Modais**                 | Botão direto nos modais de Cartas, Pacotes e Conquistas para buscar e vincular uma imagem da galeria sem precisar fazer novo upload.                      |

***

### 🛠️ Como Utilizar no Dia a Dia

{% stepper %}
{% step %}
#### Acessar a Galeria no Painel

1. Clique em **Galeria** (ícone de galeria de imagens 🖼️).
2. Todas as mídias cadastradas no programa serão carregadas instantaneamente com suas respectivas miniaturas e metadados.
{% endstep %}

{% step %}
#### Filtrar e Localizar Arquivos

* Use as abas superiores para focar em uma categoria específica (ex: clique em **Cartas** para ocultar sons e pacotes).
* Digite qualquer termo na barra **Buscar por nome...** para achar arquivos rapidamente.
* Selecione uma extensão no menu suspenso para filtrar por formato (ex: apenas arquivos `.mp3`).
{% endstep %}

{% step %}
#### Inspecionar ou Ouvir um Arquivo

* **Para Imagens:** Clique no card da imagem para abrir o modal de detalhes com visualização ampliada, dimensões e atalho para copiar a URL.
* **Para Áudios:** Pressione o botão circular **Play** no card do som para ouvi-lo na hora, ou ajuste o volume pelo controle deslizante.
{% endstep %}

{% step %}
#### Fazer Upload de Novos Arquivos

* **Direto na Galeria:** Clique no botão **"Fazer Upload"** no topo da página, escolha a categoria de destino e selecione o arquivo.
* **Ao Criar Cartas ou Pacotes:** Nas telas de criação de Cartas (`/cards`) ou Pacotes (`/packs`), ao selecionar uma imagem, o sistema agora envia automaticamente para a subpasta correspondente (`/uploads/cards` ou `/uploads/packs`).
{% endstep %}

{% step %}
#### Buscar Imagem da Galeria nos Modais de Criação

1. Ao criar ou editar uma Carta, Pacote ou Conquista, localize a seção de imagem.
2. Clique no botão **"Galeria"** (ao lado do campo de texto) ou em **"Buscar arquivo da Galeria"** (no centro da caixa de upload).
3. A janela da galeria abrirá já filtrada para a categoria relevante (ex: Cartas).
4. Use o campo de busca em tempo real ou alterne entre as abas se desejar usar uma imagem de outra categoria.
5. Clique na imagem desejada para vinculá-la imediatamente ao seu item!
{% endstep %}

{% step %}
#### Adicionar ou Organizar Arquivos em Lote pelo Windows

1. Na Galeria, clique no botão **"Abrir Pasta de Uploads"** (ícone de pasta 📂).
2. O **Windows Explorer** abrirá instantaneamente na pasta de uploads.
3. Arraste quantas imagens ou sons desejar diretamente para as pastas `cards/`, `packs/` ou `sounds/`.
4. Volte à Galeria e clique no botão **Recarregar** (ícone 🔄) para atualizar a lista.
{% endstep %}
{% endstepper %}

***

### 🌐 Integração com Overlays do OBS e API

Todos os arquivos da galeria são servidos pelo servidor interno do Baralhada Bot (porta `3000` por padrão):

```
http://localhost:PORTA/uploads/<categoria>/<nome_do_arquivo>
```

#### Exemplos de URLs Válidas:

* **Carta:** `http://localhost:PORTA/uploads/cards/dragao_dourado.png`
* **Pacote:** `http://localhost:PORTA/uploads/packs/booster_lendario.webp`
* **Som de Notificação:** `http://localhost:PORTA/uploads/sounds/pack_open.mp3`

{% hint style="info" %}
Em seus **Overlays Customizados do OBS**, você pode referenciar imagens e sons usando tanto o caminho absoluto (`http://localhost:PORTA/uploads/...`) quanto o caminho relativo (`/uploads/...`), garantindo compatibilidade total com navegadores locais e fontes de navegador do OBS.
{% endhint %}

***

### ⚡ Especificações e Recomendações de Mídia

Para garantir a melhor experiência na sua transmissão sem sobrecarregar a memória do OBS Studio ou do navegador, siga estas recomendações:

| Tipo de Mídia             | Formatos Suportados            | Formato Recomendado | Dimensões Ideais                      | Dica de Otimização                                                             |
| ------------------------- | ------------------------------ | ------------------- | ------------------------------------- | ------------------------------------------------------------------------------ |
| **Ilustrações de Cartas** | PNG, JPG, JPEG, WEBP, GIF, SVG | **PNG** ou **WEBP** | 600 × 840 px (proporção vertical 5:7) | Use fundo transparente quando a arte não cobrir toda a moldura da carta.       |
| **Capas de Pacotes**      | PNG, JPG, JPEG, WEBP, GIF      | **PNG** ou **WEBP** | 400 × 600 px ou 500 × 500 px          | Utilize compressão WEBP para carregamento instantâneo em transmissões ao vivo. |
| **Efeitos Sonoros**       | MP3, WAV, OGG, M4A, AAC        | **MP3** ou **OGG**  | N/A (Duração ideal: 1s a 6s)          | Normalize o volume para evitar picos desagradáveis de áudio na live.           |
| **Ícones / Conquistas**   | PNG, SVG, WEBP                 | **SVG** ou **PNG**  | 256 × 256 px                          | Use proporção quadrada (1:1).                                                  |

***

### 🔒 Segurança e Tratamento de Arquivos

* ✅ **Prevenção de sobrescrita acidental:** O sistema gera nomes seguros caso arquivos idênticos sejam enviados em momentos distintos.
* ✅ **Sanitização de caminhos:** As rotas da Galeria bloqueiam requisições de diretório superior (`../`) para proteger pastas sensíveis do sistema operacional.
* ✅ **Isolamento de exclusão:** Apenas arquivos contidos dentro do diretório oficial de uploads podem ser deletados através da interface.
