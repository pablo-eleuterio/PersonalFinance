# UC25 - Editar Meta Financeira

## Objetivo
Permitir que o usuário altere as informações de uma meta financeira já cadastrada.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve possuir uma meta financeira cadastrada.

## Gatilho
O usuário acessa a opção de editar uma meta financeira.

## Fluxo Principal
1. O usuário acessa a opção de editar uma meta financeira.
2. O sistema exibe as informações atuais da meta.
3. O usuário altera o nome da meta, o valor-alvo e/ou o prazo.
4. O usuário aciona a opção “Salvar”.
5. O sistema valida as informações.
6. O sistema atualiza os dados da meta financeira.
7. O sistema informa que a meta foi atualizada com sucesso.

## Fluxo de Exceção
### FE01 - Campos obrigatórios não preenchidos
1. No passo 4 do fluxo principal, o usuário aciona a opção “Salvar”.
2. Existem campos obrigatórios não preenchidos.
3. O sistema exibe uma mensagem indicando que existem campos obrigatórios não preenchidos.
4. O sistema mantém o usuário no formulário para corrigir as informações.

### FE02 - Valor-alvo inválido
1. No passo 4 do fluxo principal, o usuário aciona a opção “Salvar”.
2. O sistema identifica que o valor-alvo informado é menor ou igual a 0.
3. O sistema informa que o valor-alvo deve ser maior que 0.
4. O sistema mantém o usuário no formulário para corrigir as informações.

## Pós-condições
1. A meta financeira foi atualizada com sucesso.
2. O valor reservado da meta permanece inalterado.