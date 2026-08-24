# UC20 - Excluir Conta Financeira

## Objetivo
Permitir que o usuário exclua uma conta financeira que não possua movimentações vinculadas.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve possuir ao menos uma conta financeira cadastrada.

## Gatilho
O usuário acessa a opção de excluir conta financeira.

## Fluxo Principal
1. O usuário acessa a opção de excluir conta financeira.
2. O sistema solicita a confirmação da exclusão.
3. O usuário confirma a exclusão.
4. O sistema verifica se existem movimentações vinculadas à conta financeira.
5. O sistema identifica que a conta financeira não possui movimentações vinculadas.
6. O sistema exclui a conta financeira.

## Fluxo Alternativo
### FA01 - Usuário cancela a exclusão
1. No passo 3 do fluxo principal, o usuário cancela a exclusão.
2. O sistema mantém a conta financeira cadastrada.
3. Nenhuma alteração é realizada.

## Fluxo de Exceção
### FE01 - Conta financeira com movimentações vinculadas
1. No passo 4 do fluxo principal, o sistema identifica que a conta financeira possui movimentações vinculadas.
2. O sistema informa que a conta financeira não pode ser excluída enquanto possuir movimentações vinculadas.
3. O sistema mantém a conta financeira cadastrada.

## Pós-condições
1. A conta financeira é excluída com sucesso.