# UC17 - Excluir Meta Financeira

## Objetivo
Permitir que o usuário exclua metas financeiras.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve ter ao menos uma meta cadastrada no sistema.

## Gatilho
O usuário acessa a opção de excluir meta financeira.

## Fluxo Principal
1. O usuário acessa a opção de excluir meta financeira.
2. O sistema solicita a confirmação da exclusão da meta financeira.
3. O usuário confirma a exclusão.
4. O sistema verifica se a meta possui valor reservado.
5. O sistema não encontra nenhum valor reservado na meta.
6. O sistema exclui a meta financeira.

## Fluxo Alternativo
### FA01 - Usuário cancela a exclusão
1. No passo 3 do fluxo principal, o usuário cancela a exclusão.
2. O sistema não exclui a meta.
3. Nenhuma alteração é realizada nas metas cadastradas.  

## Fluxo de Exceção
### FE01 - Meta com valor reservado
1. No passo 4 do fluxo principal, o sistema identifica que a meta possui valor reservado.
2. O sistema informa que existe um valor reservado.
3. O sistema informa que o valor reservado deve ser retirado antes que a meta possa ser excluída.

## Pós-condições
1. A meta financeira é excluída com sucesso.


