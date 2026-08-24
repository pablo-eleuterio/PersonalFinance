# UC03 - Cadastrar Conta Financeira

## Objetivo
Permitir que o usuário faça o cadastro de uma ou mais contas financeiras.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.

## Gatilho
O usuário acessa a opção de cadastrar conta financeira.

## Fluxo Principal
1. O usuário acessa a opção de cadastrar conta financeira.
2. O sistema exibe um formulário com os campos para informar nome da conta financeira e saldo inicial.
3. O usuário preenche o formulário.
4. O usuário aciona a opção “Salvar”.
5. O sistema valida as informações.
6. O sistema cadastra a conta financeira.
7. O sistema informa que a conta financeira foi cadastrada com sucesso.

## Fluxo de Exceção
### FE01 - Nome da conta já existente
1. No passo 5 do fluxo principal, o sistema valida as informações.
2. O sistema identifica que já existe uma conta financeira com esse nome.
3. O sistema exibe uma mensagem informando que já existe uma conta financeira com esse nome.
4. O sistema mantém o usuário no passo 2 do fluxo principal até que seja informado um nome de conta financeira que não esteja cadastrado.

### FE02 - Campos obrigatórios não preenchidos
1. No passo 4 do fluxo principal, o usuário aciona a opção "Salvar".
2. Existem campos obrigatórios não preenchidos.
3. O sistema exibe uma mensagem informando que há campos obrigatórios não preenchidos.
4. O sistema mantém o usuário no passo 2 do fluxo principal até que todos os campos obrigatórios sejam preenchidos.

## Pós-condições
1. A conta financeira foi cadastrada com sucesso.
