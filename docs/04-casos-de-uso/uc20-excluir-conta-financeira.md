# UC20 - Excluir Conta Financeira

## Objetivo
Permitir que o usuário exclua uma conta financeira que não possua movimentações vinculadas.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve possuir ao menos uma conta financeira cadastrada.

## Gatilho
O usuário acessa a opção de excluir uma conta financeira.

## Fluxo Principal
1. O usuário acessa a opção de excluir uma conta financeira.
2. O sistema solicita a confirmação da exclusão.
3. O usuário confirma a exclusão.
4. O sistema verifica se a conta possui movimentações vinculadas.
5. O sistema exclui a conta financeira.
6. O sistema informa que a conta foi excluída com sucesso.

## Fluxo Alternativo
### FA01 - Conta com movimentações vinculadas
1. No passo 4 do fluxo principal, o sistema identifica que a conta possui movimentações vinculadas.
2. O sistema informa que a conta não pode ser excluída e oferece a opção de desativá-la.
3. O usuário escolhe desativar a conta.
4. O sistema desativa a conta financeira, preservando seu saldo e histórico de movimentações.
5. O sistema informa que a conta foi desativada com sucesso.

## Pós-condições
1. A conta financeira é excluída definitivamente caso não possua movimentações vinculadas; ou
2. A conta financeira é desativada caso possua movimentações e o usuário escolha desativá-la.