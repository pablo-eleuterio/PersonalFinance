# UC01 - Cadastrar Usuário

## Objetivo
Permitir que um visitante realize seu cadastro no sistema, criando uma conta para utilizar as funcionalidades de gerenciamento financeiro.

## Ator Principal
Visitante.

## Pré-condições
1. O visitante não deve possuir uma conta cadastrada no sistema.
2. O sistema deve estar disponível para realizar o cadastro.

## Gatilho
O visitante seleciona a opção de cadastro no sistema.

## Fluxo Principal
1. O visitante acessa a opção de cadastro.
2. O sistema exibe o formulário de cadastro.
3. O visitante informa os dados solicitados.
4. O visitante confirma o cadastro.
5. O sistema valida os dados informados.
6. O sistema cria a conta do usuário.
7. O sistema confirma que o cadastro foi realizado com sucesso.

## Fluxo de Exceção
### FE01 - E-mail ou telefone já cadastrado
1. No passo 5 do fluxo principal, o sistema identifica que o e-mail ou telefone informado já está cadastrado.
2. O sistema informa ao visitante que o e-mail ou telefone já está em uso.
3. O sistema solicita que o visitante informe outro e-mail ou telefone.
4. O fluxo retorna ao passo 3 do fluxo principal.

### FE02 - Dados inválidos
1. No passo 5 do fluxo principal, o sistema verifica se os dados informados são válidos.
2. O sistema identifica que um ou mais dados informados são inválidos.
3. O sistema pede para que o visitante informe novos dados.
4. O fluxo retorna ao passo 3 do fluxo principal.

## Pós-condições
1. O usuário foi cadastrado com sucesso no sistema.
2. O usuário teve seus dados armazenados.
3. O usuário está apto a realizar autenticação utilizando o e-mail ou telefone cadastrado.