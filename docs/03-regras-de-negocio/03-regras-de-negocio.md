# Regras de Negócio

## RN01 - Saldo negativo
O sistema deverá permitir o registro de despesas mesmo quando o saldo da conta se tornar negativo, refletindo a situação financeira real do usuário.

## RN02 - Categoria obrigatória
Toda receita e despesa deverá estar vinculada a uma categoria antes de ser registrada no sistema.

## RN03 - Registro de movimentações
Toda receita e despesa deverá estar vinculada a uma conta financeira. Após o registro da movimentação, o sistema deverá atualizar automaticamente o saldo da conta e o saldo consolidado do usuário.

## RN04 - Reserva de valores para metas financeiras
O sistema deverá permitir que o usuário reserve valores disponíveis de uma conta financeira para uma meta financeira. Cada reserva deverá manter a identificação da conta de origem e seu respectivo valor. O valor reservado será descontado do saldo disponível da conta selecionada e do saldo consolidado disponível. Ao retirar uma reserva, o valor deverá retornar ao saldo disponível da conta de origem.

## RN05 - Exclusão e desativação de contas financeiras
Uma conta financeira que não possua movimentações ou reservas vinculadas poderá ser excluída definitivamente. Caso a conta possua movimentações ou reservas, ela não poderá ser excluída, podendo apenas ser desativada, preservando seu histórico de movimentações. Uma conta desativada poderá ser reativada posteriormente.

## RN06 - Valor mínimo da meta financeira
O valor da meta financeira deverá ser maior que zero.

## RN07 - Edição e exclusão de movimentações
O sistema deverá permitir a edição e a exclusão de receitas e despesas cadastradas. Quando uma movimentação que já tenha impactado o saldo for editada ou excluída, o sistema deverá atualizar os saldos afetados. A edição ou exclusão de despesas previstas não deverá alterar os saldos enquanto elas não tiverem sido marcadas como pagas.

## RN08 - Nome único da conta financeira
O sistema não deverá permitir que um usuário cadastre mais de uma conta financeira com o mesmo nome.

## RN09 - Valor da movimentação
O valor de toda receita e despesa deverá ser maior que zero.

## RN10 - Despesas previstas
Uma despesa prevista não deverá alterar o saldo da conta financeira. A despesa permanecerá como prevista mesmo após a data informada e somente afetará o saldo quando o usuário marcá-la como paga.

## RN11 – Edição de categoria
Ao editar o nome de uma categoria, a alteração deverá ser refletida em todas as receitas e despesas vinculadas a essa categoria.

## RN12 – Exclusão de categoria
Uma categoria vinculada a receitas ou despesas não deverá ser excluída definitivamente, devendo ser desativada para novos lançamentos e mantida nos registros já existentes.

## RN13 – Reativação de categoria
Se o usuário tentar cadastrar uma categoria com o mesmo nome de uma categoria desativada, o sistema deverá permitir a reativação da categoria existente, em vez de criar uma nova categoria.

## RN14 – Prazo da meta financeira
O prazo para conclusão de uma meta financeira será opcional.

## RN15 – Múltiplas metas financeiras
O usuário poderá possuir mais de uma meta financeira ativa simultaneamente.

## RN16 - Exclusão de meta financeira
Uma meta financeira que possua valor reservado não poderá ser excluída. O usuário deverá retirar todo o valor reservado antes de realizar a exclusão.

## RN17 - Recuperação de senha
A redefinição de senha deverá ocorrer por meio de um código ou link temporário enviado para um meio de contato previamente cadastrado pelo usuário. O código ou link deverá possuir validade limitada e não poderá ser reutilizado após a redefinição da senha.

### RN18 - Repetição mensal de despesas
O usuário poderá definir uma quantidade de repetições mensais ao cadastrar uma despesa. A primeira despesa será registrada na data informada e as demais serão geradas nos meses seguintes, mantendo a mesma conta financeira, categoria, valor e descrição. As despesas futuras geradas pela repetição serão cadastradas com o status "Prevista" e não afetarão o saldo até serem marcadas como pagas.

## RN19 - Contas financeiras desativadas
Uma conta financeira desativada não poderá ser utilizada em novas movimentações e seu saldo não será considerado no cálculo do saldo consolidado. A desativação não deverá alterar o saldo registrado nem o histórico de movimentações da conta. Ao ser reativada, seu saldo voltará a ser considerado no saldo consolidado.

## RN20 - Alteração do saldo inicial
O saldo inicial de uma conta financeira poderá ser alterado enquanto a conta não possuir movimentações vinculadas. Após o registro da primeira movimentação, o saldo inicial não poderá mais ser alterado.