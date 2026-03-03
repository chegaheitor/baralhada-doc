# 🚧 Especificações Técnicas

Esta seção é dedicada ao detalhamento da "engrenagem" que faz o Baralhada Bot funcionar. Aqui, desenvolvedores e usuários avançados podem entender como o sistema gerencia conexões, lida com erros e se comunica com a Twitch.

***

### 🏗️ O que você encontrará nesta categoria

A documentação técnica está dividida em três pilares fundamentais:

#### 1. Arquitetura e Conectividade

* **O Coração do Sistema:** Como o servidor Node.js e a interface Electron trabalham juntos.
* **Portas Dinâmicas:** Entenda como o arquivo `port.json` permite que o frontend e o backend se encontrem automaticamente.
* **Segurança Local:** Detalhes sobre a comunicação via `localhost`.

#### 2. Diagnóstico e Saúde do Sistema

* **Interceptação de Logs:** Como o bot captura mensagens de erro de bibliotecas externas (`stdout/stderr`) e as exibe no console.
* **Categorias de Eventos:** Explicação sobre os logs de sistema, banco de dados e conexão.
* **Resolução de Problemas:** Ferramentas integradas para identificar falhas de comunicação com a Twitch.

#### 3. Integração com a API da Twitch

* **Helix API:** Como o bot usa a API moderna da Twitch para buscar fotos de perfil e verificar status do canal.
* **Gerenciamento de Tokens:** O fluxo automático de atualização e validação do Client ID e App Access Tokens.
* **Performance:** Como otimizamos as requisições para evitar limites de taxa (Rate Limits).

***

### 🛠️ Tecnologias Utilizadas

Para curiosidade técnica, o Baralhada utiliza um stack moderno e leve:

* **Backend:** Node.js com Express.
* **Frontend:** React com Vite e Tailwind CSS.
* **Banco de Dados:** NeDB (NoSQL baseado em arquivos local).
* **Desktop:** Electron para empacotamento.

{% hint style="info" %}
Esta documentação é voltada para transparência técnica. Para a maioria dos usuários, o bot funciona de forma automática ("plug and play"), sem necessidade de alteração nestes arquivos internos.
{% endhint %}
