# Regras de Negócio

## RN01 - Saldo negativo
O sistema deverá permitir o registro de despesas mesmo quando o saldo da conta se tornar negativo, refletindo a situação financeira real do usuário.

## RN02 - Categoria obrigatória
Toda receita e despesa deverá estar vinculada a uma categoria antes de ser registrada no sistema.

## RN03 - Registro de movimentações
Toda receita e despesa deverá estar vinculada a uma conta financeira. Após o registro da movimentação, o sistema deverá atualizar automaticamente o saldo da conta e o saldo consolidado do usuário.

## RN04 - Reserva de valores para metas financeiras
O sistema deverá permitir que o usuário reserve valores disponíveis de uma conta financeira para uma meta financeira e retire valores previamente reservados. O valor reservado deverá ser descontado do saldo da conta financeira selecionada e do saldo consolidado. Ao retirar um valor reservado, o valor deverá retornar para a conta financeira selecionada e o saldo consolidado deverá ser atualizado.

## RN05 - Exclusão de contas financeiras
O sistema não deverá permitir a exclusão de uma conta financeira que possua movimentações vinculadas.

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