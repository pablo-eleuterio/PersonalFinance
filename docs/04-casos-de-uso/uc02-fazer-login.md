# UC02 - Fazer Login

## Objetivo
Permitir que o usuário cadastrado realize o login e acesse as funcionalidades do sistema.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário estar cadastrado no nosso sistema

## Gatilho
O usuário clica na opção de fazer login.

## Fluxo Principal
1. O usuário acessa a opção de fazer login.
2. O sistema exibe um formulário com e-mail/telefone e senha para o usuário.
3. O usuário preenche os dados solicitados.
4. O usuário aciona o botão "Entrar".
5. O sistema verifica os dados informados pelo usuário.
6. O usuário é autenticado.
7. O sistema direciona o usuário para o Dashboard.

## Fluxo de Exceção
### FE01 - Dados inválidos
1. No passo 5 do fluxo principal, o sistema verifica os dados informados pelo usuário.
2. Os dados informados não correspondem aos dados cadastrados no sistema.
3. O sistema exibe uma mensagem informando que o login não pôde ser realizado.
4. O usuário é redirecionado para o passo 2 do fluxo principal.

### FE02 - Campos obrigatórios não preenchidos
1. No passo 4 do fluxo principal, o usuário clica no botão "Entrar".
2. Existem campos obrigatórios não preenchidos.
3. O sistema exibe uma mensagem informando que não foi possível realizar o login, pois há campos obrigatórios não preenchidos.
4. O sistema mantém o usuário no passo 2 do fluxo principal até que os campos obrigatórios sejam preenchidos.

## Pós-condições
1. O usuário foi autenticado com sucesso.
2. O usuário é direcionado ao Dashboard do sistema.
