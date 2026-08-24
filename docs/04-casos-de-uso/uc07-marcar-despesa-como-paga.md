# UC07 - Marcar Despesa como Paga

## Objetivo
Permitir que o usuário altere o status de uma despesa prevista para paga.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.

## Gatilho
O usuário seleciona a opção de marcar como paga.

## Fluxo Principal
1. O usuário seleciona a opção marcar como paga na despesa escolhida.
2. O sistema solicita a confirmação do pagamento da despesa.
3. O usuário confirma o pagamento.
4. O sistema altera o status da despesa para paga.
5. O sistema desconta o valor da despesa do saldo da conta financeira vinculada.
6. O sistema atualiza o saldo total do usuário.
7. O sistema exibe uma mensagem informando que a despesa foi marcada como paga com sucesso.

## Fluxo Alternativo
### FA01 - Usuário cancela pagamento
1. No passo 3 do fluxo principal, o usuário cancela o pagamento.
2. O sistema mantém a despesa com o status de prevista.
3. O sistema retorna o usuário à consulta de despesas previstas.

## Pós-condições
1. A despesa é marcada como paga.
2. O valor da despesa é descontado do saldo da conta financeira vinculada.
3. O saldo total do usuário é atualizado.

