# UC23 - Redefinir Senha

## Objetivo
Permitir que o usuário redefina sua senha caso não consiga acessar sua conta.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve possuir uma conta cadastrada no sistema.
2. O usuário deve possuir um meio de contato válido cadastrado no sistema.

## Gatilho
O usuário acessa a opção de recuperação de senha.

## Fluxo Principal
1. O usuário acessa a opção de recuperação de senha.
2. O sistema solicita um meio de identificação da conta.
3. O usuário informa os dados solicitados.
4. O usuário confirma a solicitação de recuperação.
5. O sistema valida os dados informados.
6. O sistema envia um código ou link temporário de recuperação para o meio de contato cadastrado.
7. O usuário acessa o processo de redefinição de senha.
8. O sistema solicita a nova senha.
9. O usuário informa e confirma a nova senha.
10. O sistema valida a nova senha.
11. O sistema armazena a nova senha utilizando um algoritmo seguro de hash.
12. O sistema invalida o código ou link utilizado na recuperação.
13. O sistema informa que a senha foi redefinida com sucesso.

## Fluxo de Exceção
### FE01 - Conta não encontrada
1. No passo 4 do fluxo principal, o usuário confirma a solicitação com dados que não correspondem a uma conta cadastrada.
2. O sistema identifica que a conta não foi encontrada.
3. O sistema informa que não foi possível prosseguir com a recuperação.
4. O sistema mantém o usuário na opção de recuperação de senha.

### FE02 - Código ou link inválido ou expirado
1. No passo 7 do fluxo principal, o sistema identifica que o código ou link de recuperação é inválido ou expirou.
2. O sistema informa que o processo de recuperação não é mais válido.
3. O sistema permite que o usuário solicite uma nova recuperação de senha.

### FE03 - Nova senha inválida
1. No passo 9 do fluxo principal, o usuário confirma uma nova senha que não atende aos critérios definidos pelo sistema.
2. O sistema identifica que a nova senha é inválida.
3. O sistema informa que a senha deve atender aos critérios de segurança.
4. O sistema mantém o usuário na etapa de redefinição para informar uma nova senha.

## Pós-condições
1. A senha anterior deixa de ser válida.
2. A nova senha é armazenada de forma segura no sistema.
3. O código ou link utilizado na recuperação é invalidado.