# Cartas

## 🃏 O que é uma Carta

As cartas são o coração do seu jogo de TCG. Elas representam os itens colecionáveis que os viewers buscam resgatar, trocar e exibir. Cada carta tem atributos únicos como raridade, tipos, atributos e imagem.

## 🔢 Criando uma Carta

{% stepper %}
{% step %}
### Vá em Painel → Cartas

Acesse a área de gerenciamento de cartas no painel administrativo.
{% endstep %}

{% step %}
### Clique em Nova Carta

Inicie a criação de uma nova carta.
{% endstep %}

{% step %}
### Preencha os campos

Complete o formulário com as informações da carta:

<table><thead><tr><th width="135">Campo</th><th width="126">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><a href="cartas.md#nome"><strong>Nome</strong></a></td><td>✅</td><td>O nome oficial da carta (ex: "Dragão Supremo").</td></tr><tr><td><a href="cartas.md#slugs"><strong>Slug</strong></a></td><td>✅</td><td>Identificador único gerado automaticamente, versão curta do nome sem espaços usada em comandos (ex: <code>dragao_supremo</code>).</td></tr><tr><td><a href="cartas.md#numero-do-album"><strong>Número de Álbum</strong></a></td><td>✅</td><td>A posição da carta na coleção (ex: #001).</td></tr><tr><td><a href="cartas.md#colecao"><strong>Coleção</strong></a></td><td>—</td><td>Nome da coleção à qual pertence. </td></tr><tr><td><a href="cartas.md#raridades"><strong>Raridade</strong></a></td><td>✅</td><td>Define o quão difícil é encontrar essa carta. </td></tr><tr><td><a href="cartas.md#tipagem"><strong>Tipo</strong></a></td><td>✅</td><td>Tipo primário (ex: Fogo, Água, Terra)</td></tr><tr><td><strong>Tipo 2</strong></td><td>—</td><td>Tipo secundário opcional</td></tr><tr><td><a href="cartas.md#atributos"><strong>HP</strong></a></td><td>—</td><td>Pontos de vida (cosmético).</td></tr><tr><td><strong>Ataque</strong></td><td>—</td><td>Pontos de ataque (cosmético).</td></tr><tr><td><strong>Defesa</strong></td><td>—</td><td>Pontos de defesa (cosmético).</td></tr><tr><td><a href="cartas.md#imagem"><strong>Imagem</strong></a></td><td>—</td><td>URL ou upload direto de arquivo.</td></tr><tr><td><strong>Ativa</strong></td><td>—</td><td>Pode ser resgatada em um pacote.</td></tr></tbody></table>
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Gerenciando Cartas

* **Filtrar:** Pesquise por nome, coleção, tipo ou raridade
* **Editar:** Clique no ícone de lápis
* **Excluir:** Clique no ícone de lixeira (irreversível)
* **Upload de Imagem:** Arraste ou selecione um arquivo na tela de edição
{% endhint %}

## 🔠 Nome

É o nome exibido em destaque no topo da carta e em todas as mensagens do chat.

* **Impacto**: O nome define a identidade do item. Tente nomes épicos ou divertidos que façam sentido para a sua comunidade.
* **Dica**: Nomes muito longos podem ser cortados visualmente em resoluções menores do overlay.

## 🆔 Slugs (ID Amigável)

O "ID de Chat" da carta. É o que o viewer digita em comandos como `!carta <slug>` ou `!vender <slug>`.

O slug é gerado automaticamente a partir do nome (espaços viram `_`, caracteres especiais removidos). Pode ser editado manualmente. Deve ser único entre todas as cartas. Exemplo: "Ave de Fogo" → `ave_de_fogo`.

* **Impacto**: Afeta diretamente a usabilidade. Se o slug for `ave_de_fogo_muito_forte`, o viewer terá dificuldade de digitar.

## 🔢 Número do Álbum

A numeração oficial da carta dentro de um set.

* **Impacto**: Crucial para o comando `!album`. Se você tiver duas cartas com o mesmo número na mesma coleção, a visualização da grade pode apresentar erros.
* **Organização**: Pense nisso como o número da figurinha. Ajuda o viewer a saber se falta a "número 1" ou a "número 50" para completar a coleção.

## 📦 Coleção&#x20;

Agrupa as cartas sob um tema comum.

* **Origem**: As opções são preenchidas automaticamente com os pacotes criados na página de **Pacotes**.
* **Impacto**: Define onde a carta "mora". Você pode criar Pacotes que dropam apenas cartas da "Coleção Gênesis", por exemplo.
* **Vantagem**: Facilita a criação de eventos sazonais (Natal, Halloween, Aniversário do Canal).

## 💎 Raridades

Determina a distribuição e a importância da carta e a chance de ela aparecer em pacotes.

* **Origem**: As opções disponíveis são as raridades criadas na página de **Personalização**.
* **Impacto**:
  * **Visual**: Cada raridade tem uma cor/estilo de borda diferente no overlay.
  * **Algoritmo**: O sistema de abertura de pacotes usa as chances de raridade (odds) para decidir qual carta entregar.
* **Progresso**: Viewers sentem muito mais impacto ao tirar uma "Lendária" devido ao alerta especial no overlay.

## 🏷 Tipagem

Categorias ou elementos da carta (ex: Fogo, Humano, Veículo, Streamer).

* **Origem**: As opções de tipos são as que foram criadas na página de **Personalização**.
* **Impacto**: Atrai colecionadores por nicho. O bot exibe ícones automáticos baseados nos tipos detectados, dando um ar profissional à resposta do chat.
* **Dica**: Você pode definir até dois tipos por carta para criar combinações interessantes (ex: `Fogo` | Veículo).

## 📊 Atributos

Os números de "poder" da carta.

* **Impacto**: Atualmente servem para comparação e prestígio no chat. No futuro, podem ser usados em sistemas de batalha automática entre viewers.
* **Equilíbrio**: Cartas lendárias devem ter atributos significativamente maiores para justificar sua raridade.

## 🖼 Imagem

A "alma" da carta. O bot aceita arquivos locais ou links externos.

* **Impacto**: Define o "WOW" factor da live. Quando um viewer abre um pacote, a imagem aparece em tamanho grande na tela.
* **Melhores Práticas**:
  * Use imagens horizontais ou verticais consistentes.
  * **PNG com Transparência**: Ative o segredo de ouro! Artes com fundo transparente ficam muito mais profissionais integradas ao layout do overlay.
  * **Tamanho**: Mantenha as imagens leves (abaixo de 500kb) para que o overlay carregue instantaneamente durante a live.

{% hint style="info" %}
**Planejamento é tudo!** Antes de criar 100 cartas, crie 5 "pilotos" (uma de cada raridade) e teste como elas aparecem na sua live usando o comando `!carta <slug>`. Isso garante que o tamanho da arte e as cores estão perfeitos para seu setup.
{% endhint %}
