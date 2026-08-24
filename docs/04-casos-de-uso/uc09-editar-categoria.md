# UC09 - Editar Categoria

## Objetivo
Permitir que o usuário edite o nome de uma categoria já cadastrada.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve ter ao menos uma categoria cadastrada.

## Gatilho
O usuário acessa a opção de editar categoria.

## Fluxo Principal
1. O usuário acessa a opção de editar categoria.
2. O sistema exibe o campo com o nome atual da categoria.
3. O usuário informa o novo nome da categoria.
4. O usuário confirma a edição.
5. O sistema valida o novo nome.
6. O sistema renomeia a categoria.

## Fluxo de Exceção
### FE01 - Campo vazio
1. No passo 4 do fluxo principal, o usuário confirma a edição com o campo vazio.
2. O sistema identifica que o campo não foi preenchido.
3. O sistema informa que o nome da categoria deve ser preenchido.
4. O sistema mantém o usuário no campo para informar um novo nome para a categoria.

### FE02- Nome de categoria já existente
1. No passo 4 do fluxo principal, o usuário confirma a edição com um nome já utilizado por outra categoria.
2. O sistema identifica que o nome informado já existe.
3. O sistema informa que não é possível utilizar o nome de uma categoria já existente.
4. O sistema mantém o usuário no campo para informar um novo nome para a categoria.

## Pós-condições
1. A categoria é renomeada com sucesso.
2. O novo nome da categoria passa a ser refletido nas receitas e despesas vinculadas a ela.