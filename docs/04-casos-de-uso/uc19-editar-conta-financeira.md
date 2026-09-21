# UC19 - Editar Conta Financeira

## Objetivo
Permitir que o usuário edite as informações de uma conta financeira cadastrada.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve possuir ao menos uma conta financeira cadastrada.

## Gatilho
O usuário acessa a opção de editar conta financeira.

## Fluxo Principal
1. O usuário acessa a opção de editar conta financeira.
2. O sistema exibe as informações atuais da conta financeira selecionada.
3. O usuário altera o nome da conta e, caso a conta não possua movimentações vinculadas, poderá alterar também o saldo inicial.
4. O usuário confirma a edição.
5. O sistema valida as informações.
6. O sistema atualiza a conta financeira.

## Fluxo de Exceção
### FE01 - Campos obrigatórios não preenchidos
1. No passo 4 do fluxo principal, o usuário confirma a edição sem preencher um ou mais campos obrigatórios.
2. O sistema identifica os campos obrigatórios não preenchidos.
3. O sistema informa que os campos obrigatórios devem ser preenchidos.
4. O sistema mantém o usuário na opção de edição para corrigir as informações.

## Pós-condições
1. As informações da conta financeira são atualizadas com sucesso.