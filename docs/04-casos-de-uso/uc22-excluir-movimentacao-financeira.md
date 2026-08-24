# UC22 - Excluir Movimentação Financeira

## Objetivo
Permitir que o usuário exclua uma movimentação financeira cadastrada.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve possuir ao menos uma movimentação financeira cadastrada.

## Gatilho
O usuário seleciona a opção de excluir uma movimentação financeira no histórico de transações ou na consulta de despesas previstas.

## Fluxo Principal
1. O usuário acessa a opção de excluir uma movimentação financeira.
2. O sistema solicita a confirmação da exclusão.
3. O usuário confirma a exclusão.
4. O sistema verifica se a movimentação já impactou o saldo.
5. O sistema exclui a movimentação financeira.
6. Caso a movimentação tenha impactado o saldo, o sistema atualiza os saldos afetados.

## Fluxo Alternativo
### FA01 - Usuário cancela a exclusão
1. No passo 3 do fluxo principal, o usuário cancela a exclusão.
2. O sistema não exclui a movimentação financeira.
3. Nenhuma alteração é realizada nos saldos.

## Pós-condições
1. A movimentação financeira é excluída com sucesso.
2. Os saldos afetados são atualizados quando necessário.