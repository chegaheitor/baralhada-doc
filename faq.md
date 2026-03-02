# FAQ

## 🔧 Configuração

<details>

<summary><strong>O bot conecta mas não responde no chat. O que fazer?</strong></summary>

Verifique se o token OAuth está correto e se o nome de usuário do bot bate com a conta do token gerado. O token deve ser gerado logado na conta do **bot**, não na sua conta pessoal.

</details>

<details>

<summary><strong>"No response from Twitch" aparece nos logs. É erro?</strong></summary>

Não necessariamente. É uma mensagem de timeout temporária do IRC do Twitch. O bot tenta reconectar automaticamente e geralmente se normaliza sozinho.

</details>

<details>

<summary><strong>Preciso deixar o computador ligado?</strong></summary>

Sim. O Baralhada Bot roda localmente na sua máquina. O bot só funciona enquanto o programa estiver aberto e o computador ligado.

</details>

## 🃏 Cartas e Pacotes

<details>

<summary><strong>Posso ter cartas sem coleção?</strong></summary>

Sim, o campo de coleção é opcional. Cartas sem coleção não aparecem no progresso de álbum.

</details>

<details>

<summary><strong>Como as chances de raridade funcionam?</strong></summary>

Cada pacote tem porcentagens por raridade (ex: Comum 60%, Incomum 25%, Rara 10%, Épica 4%, Lendária 1%). Quando aberto, o sistema sorteia uma raridade com base nessas chances e então escolhe uma carta aleatória dessa raridade.

</details>

<details>

<summary><strong>Se o pacote não tiver cartas de uma raridade sorteada, o que acontece?</strong></summary>

O sistema tenta novamente com outra raridade. Se não encontrar cartas disponíveis, a mensagem `open_empty` é exibida.

</details>

## 💬 Comandos

<details>

<summary><strong>Posso mudar o prefixo dos comandos (de `!` para outro caractere)?</strong></summary>

Não nativamente. O `!` está hardcoded como prefixo. Mas você pode mudar o **trigger** de cada comando (ex: mudar `claim` para `pegar` → usuários digitam `!pegar`).

</details>

<details>

<summary><strong>Como impedir que um comando seja usado por não-subscribers?</strong></summary>

Na configuração do comando, mude a **Permissão Mínima** para `sub`. Apenas assinantes e acima poderão usar o comando.

</details>

<details>

<summary><strong>O que é "slug" em cartas e pacotes?</strong></summary>

É o identificador único sem espaços ou caracteres especiais. Usado internamente para identificar itens sem ambiguidade. Exemplo: carta "Dragão de Fogo" → slug `dragao_de_fogo`.

</details>

## 🔄 Trades

<details>

<summary><strong>O usuário pode se recusar a ver uma proposta de troca?</strong></summary>

Sim — usando `!tradeOffer recusar`. A troca é cancelada e ambos os usuários são notificados.

</details>

<details>

<summary><strong>As trocas têm tempo limite?</strong></summary>

Sim. A oferta expira após alguns segundos sem resposta (configurável no código). Se expirar, a troca é cancelada automaticamente.

</details>

## 💾 Dados e Backup

<details>

<summary><strong>Onde ficam os dados do programa?</strong></summary>

```
Windows: C:\Users\[SeuNome]\AppData\Roaming\baralhada-bot\
```

</details>

<details>

<summary><strong>Se eu reinstalar o programa, perco os dados?</strong></summary>

Não, desde que a pasta `AppData/Roaming/baralhada-bot` não seja deletada. Os dados ficam separados da instalação do programa.

</details>

<details>

<summary><strong>Posso usar o mesmo banco de dados em outro computador?</strong></summary>

Sim. Copie a pasta `baralhada-bot` do AppData para o mesmo local no outro computador.

</details>

## 📊 Estatísticas e Logs

<details>

<summary><strong>Os logs somem quando fecho o programa?</strong></summary>

Os logs em tempo real no Dashboard são voláteis (apenas na sessão atual). Logs persistentes ficam nos arquivos de log na pasta de dados da aplicação.

</details>
