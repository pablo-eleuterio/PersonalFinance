# UC04 - Cadastrar Receita

## Objetivo
Permitir que o usuário faça o cadastro de suas receitas e as vincule a uma conta financeira.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.

## Gatilho
O usuário acessa a opção de cadastrar receita. 

## Fluxo Principal
1. O usuário acessa a opção de cadastrar receita.
2. O sistema exibe um formulário com os campos para informar a conta financeira, o valor, a data, a categoria e a descrição da receita.
3. O usuário preenche o formulário.
4. O usuário aciona a opção “Salvar”.
5. O sistema valida as informações.
6. O sistema cadastra a receita.
7. O sistema informa que a receita foi cadastrada com sucesso.

## Fluxo de Exceção
### FE01 - Campos obrigatórios não preenchidos
1. No passo 4 do fluxo principal, o usuário aciona a opção "Salvar".
2. Existem campos obrigatórios não preenchidos.
3. O sistema exibe uma mensagem indicando que existem campos obrigatórios não preenchidos.
4. O sistema mantém o usuário no passo 2 do fluxo principal até que todos os campos obrigatórios sejam preenchidos.

### FE02 - Valor inválido
1. No passo em que o usuário confirma o cadastro da receita, o usuário confirma o cadastro com um valor menor ou igual a 0.
2. O sistema identifica que o valor informado é inválido.
3. O sistema informa que o valor da receita deve ser maior que 0.
4. O sistema mantém o usuário no formulário para corrigir as informações.

## Pós-condições
1. A receita foi cadastrada com sucesso.



