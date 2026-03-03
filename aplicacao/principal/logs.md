# Logs

## 📜 O que são os Logs?

Diferente do Console (que foca no sistema), os Logs focam nas **ações dos usuários**. Cada vez que uma ação acontece no programa, uma entrada é registrada aqui permanentemente.

## 🛠️ Ferramentas de Auditoria

#### 🔍 Busca e Filtros

Você não precisa ler linha por linha. Utilize as ferramentas de busca:

* **Busca por Texto:** Digite o nome de um usuário ou o nome de uma ação para filtrar instantaneamente.
* **Filtro por Ação:** Visualize apenas "Trocas", apenas "Vendas" ou apenas "Ações Administrativas".
* **Ordem Cronológica:** Alterne entre ver os eventos mais novos ou os mais antigos primeiro.

### 🧹 Limpeza do Histórico

O botão **Limpar** apaga todo o histórico de atividades.

* **Quando usar?** Recomendamos limpar no início de uma nova "Temporada" ou se o arquivo de logs estiver ficando pesado demais (acima de 50.000 entradas).

### ✨ Categorias de Logs

<table><thead><tr><th width="139">Categoria</th><th width="129" align="center">Ícone</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Compra</strong></td><td align="center">🛍️</td><td>Itens e pacotes adquiridos por usuários na loja.</td></tr><tr><td><strong>Venda</strong></td><td align="center">💰</td><td>Cartas ou pacotes vendidos por usuários para o sistema.</td></tr><tr><td><strong>Troca</strong></td><td align="center">🤝</td><td>Transações realizadas entre dois usuários (P2P).</td></tr><tr><td><strong>Abertura</strong></td><td align="center">🃏</td><td>Registro de pacotes abertos e cartas obtidas.</td></tr><tr><td><strong>Resgate</strong></td><td align="center">⚡</td><td>Sucesso ao capturar pacotes selvagens (spawns).</td></tr><tr><td><strong>Presente</strong></td><td align="center">🎁</td><td>Itens enviados diretamente de um usuário para outro.</td></tr><tr><td><strong>Daily</strong></td><td align="center">✨</td><td>Resgate de pontos diários de fidelidade.</td></tr><tr><td><strong>Dica</strong></td><td align="center">🔍</td><td>Compra de pistas para completar coleções.</td></tr><tr><td><strong>Admin</strong></td><td align="center">🛡️</td><td>Criação, edição ou exclusão de conteúdos via painel.</td></tr><tr><td><strong>Bot</strong></td><td align="center">🤖</td><td>Inicialização, parada e disparos manuais do sistema.</td></tr></tbody></table>

{% hint style="info" %}
**Dica de Moderação:** Se um viewer reclamar que "uma carta sumiu", use o filtro de busca pelo nome dele. O log nunca mente e mostrará se ele vendeu, trocou ou deu a carta de presente sem querer.
{% endhint %}

## 🔄 Auto-Limpeza de Logs

O sistema Baralhada conta com uma função de **Auto-Limpeza**, projetada para manter o banco de dados leve e o aplicativo performático em sessões longas.

* **Como funciona:**
  * **Reinicialização do Bot:** Sempre que o bot for parado e iniciado novamente (Restart), os logs são purgados automaticamente.
  * **Abertura do Programa:** Ao lançar o aplicativo Baralhada pela primeira vez na sessão, o histórico é limpo para começar do zero.
* **Vantagem:** Evita lentidão no carregamento da página de logs causada por milhares de registros acumulados de lives passadas.

{% hint style="info" %}
Ative a auto-limpeza se você percebe que a página de Logs demora a carregar. Como as estatísticas importantes ficam salvas em sua própria página, os logs servem mais para monitoramento em tempo real do que para arquivo histórico permanente.
{% endhint %}

## 💡 Dicas de Monitoramento

* **Picos de Atividade:** Fique atento aos logs de "Venda" e "Abertura" logo após um sorteio ou grande pack opening para garantir que a economia do chat está equilibrada.
* **Contexto:** Clique em um log para ver detalhes técnicos (se disponíveis), como IDs de transação e metadados da carta envolvida.
* **Sincronização:** O fluxo de logs é atualizado automaticamente a cada 5 segundos, mas você pode forçar a sincronização clicando em **"Atualizar"**.
