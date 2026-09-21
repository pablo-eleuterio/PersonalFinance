# UC16 - Retirar Valor da Meta

## Objetivo
Permitir que o usuário remova um determinado valor de uma meta financeira.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve ter ao menos uma meta cadastrada no sistema.
3. A meta selecionada deve possuir valor reservado.

## Gatilho
O usuário acessa a opção de remover valor da meta.

## Fluxo Principal
1. O usuário acessa a opção de remover valor da meta.
2. O sistema exibe as contas de origem que possuem valores reservados nessa meta e solicita o valor a ser retirado.
3. O usuário seleciona uma dessas contas e informa o valor.
4. O usuário confirma a remoção.
5. O sistema valida as informações.
6. O sistema reduz o valor reservado da meta, referente à conta selecionada.
7. O sistema devolve o valor ao saldo disponível da conta de origem.
8. O sistema atualiza o saldo consolidado disponível e o progresso da meta.

## Fluxo de Exceção
### FE01 - Valor inválido
1. No passo 4 do fluxo principal, o usuário confirma a remoção com um valor menor ou igual a 0.
2. O sistema identifica que o valor informado para a remoção é inválido.
3. O sistema informa que o valor a ser removido deve ser maior que 0.
4. O sistema mantém o usuário no formulário para corrigir as informações.

### FE02 - Valor de retirada maior que o reservado na conta selecionada
1. No passo 4 do fluxo principal, o usuário confirma a remoção com um valor maior que o valor reservado na meta.
2. O sistema identifica que o valor informado para a remoção é inválido.
3. O sistema informa que o valor a ser removido não pode ser maior que o valor reservado na meta.
4. O sistema mantém o usuário no formulário para corrigir as informações.

## Pós-condições
1. O valor é removido da meta financeira com sucesso.
2. O valor removido retorna para a conta financeira selecionada.
3. O saldo consolidado é atualizado.






