# UC13 - Criar Meta Financeira

## Objetivo
Permitir que o usuário crie suas metas financeiras.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.

## Gatilho
O usuário acessa a opção de criar meta financeira.

## Fluxo Principal
1. O usuário acessa a opção de criar meta financeira.
2. O sistema exibe um formulário com os campos para informar o nome da meta, o valor objetivo e, opcionalmente, o prazo para conclusão.
3. O usuário preenche o formulário.
4. O usuário confirma a criação da meta.
5. O sistema valida as informações.
6. O sistema cria a meta.

## Fluxo de Exceção
### FE01 - Campos obrigatórios não preenchidos
1. No passo 4 do fluxo principal, o usuário confirma a criação da meta sem preencher um ou mais campos obrigatórios.
2. O sistema identifica os campos obrigatórios não preenchidos.
3. O sistema informa que os campos obrigatórios devem ser preenchidos.
4. O sistema mantém o usuário no formulário para corrigir as informações.

### FE02 - Valor objetivo inválido
1. No passo 4 do fluxo principal, o usuário confirma a criação da meta com o valor objetivo igual ou menor que 0.
2. O sistema identifica o campo com valor inválido.
3. O sistema informa que o valor do objetivo deve ser maior que 0.
4. O sistema mantém o usuário no formulário para corrigir as informações.

## Pós-condições
1. A meta financeira é criada e fica disponível para acompanhamento.