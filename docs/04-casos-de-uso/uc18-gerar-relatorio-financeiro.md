# UC18 - Gerar Relatório Financeiro

## Objetivo
Permitir que o usuário gere e consulte seu relatório financeiro referente a um determinado período.

## Ator Principal
Usuário.

## Pré-condições
1. O usuario deve estar logado no sistema.

## Gatilho
O usuário acessa a opção de gerar relatório financeiro.

## Fluxo Principal
1. O usuário acessa a opção de gerar relatório financeiro.
2. O sistema solicita o período desejado para o relatório.
3. O usuário informa o período.
4. O usuário confirma a geração do relatório.
5. O sistema valida o período informado.
6. O sistema gera o relatório financeiro referente ao período selecionado. 
7. O sistema exibe as receitas, despesas e economia do período, além do saldo atual consolidado do usuário.

## Fluxo de Exceção
### FE01 - Período Inválido
1. No passo 4 do fluxo principal, o usuário confirma a geração do relatório com um período inválido.
2. O sistema identifica que o período informado é inválido.
3. O sistema informa ao usuário que o período deve ser corrigido.
4. O sistema mantém o usuário na opção de geração do relatório para informar um período válido.

## Pós-condições
1. O relatório financeiro referente ao período selecionado é exibido ao usuário.