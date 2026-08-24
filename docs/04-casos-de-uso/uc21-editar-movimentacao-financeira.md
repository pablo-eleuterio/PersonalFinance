# UC21 - Editar Movimentação Financeira

## Objetivo
Permitir que o usuário edite as informações de uma movimentação financeira cadastrada.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve possuir ao menos uma movimentação financeira cadastrada.

## Gatilho
O usuário seleciona a opção de editar uma movimentação financeira no histórico de transações ou na consulta de despesas previstas.

## Fluxo Principal
1. O usuário acessa a opção de editar uma movimentação financeira.
2. O sistema exibe as informações atuais da movimentação selecionada.
3. O usuário altera as informações desejadas.
4. O usuário confirma a edição.
5. O sistema valida as informações.
6. O sistema atualiza os dados da movimentação financeira.
7. Caso a movimentação já tenha impactado o saldo, o sistema recalcula os saldos afetados.

## Fluxo de Exceção
### FE01 - Campos obrigatórios não preenchidos
1. No passo 4 do fluxo principal, o usuário confirma a edição sem preencher um ou mais campos obrigatórios.
2. O sistema identifica os campos obrigatórios não preenchidos.
3. O sistema informa que os campos obrigatórios devem ser preenchidos.
4. O sistema mantém o usuário na opção de edição para corrigir as informações.

### FE02 - Valor inválido
1. No passo 4 do fluxo principal, o usuário confirma a edição com um valor menor ou igual a 0.
2. O sistema identifica que o valor informado é inválido.
3. O sistema informa que o valor da movimentação deve ser maior que 0.
4. O sistema mantém o usuário na opção de edição para corrigir as informações.

## Pós-condições
1. A movimentação financeira é atualizada com sucesso.
2. Os saldos afetados são recalculados quando necessário.
3. Caso seja uma despesa prevista, nenhum saldo é alterado.