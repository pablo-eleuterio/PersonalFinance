# UC08 - Cadastrar Categoria

## Objetivo
Permitir que o usuário cadastre categorias para serem utilizadas na classificação de receitas e despesas.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.

## Gatilho
O usuário acessa a opção cadastrar categoria.

## Fluxo Principal
1. O usuário acessa a opção de cadastrar categoria.
2. O sistema exibe um campo para informar o nome da categoria.
3. O usuário informa o nome da categoria.
4. O usuário confirma o cadastro da categoria.
5. O sistema valida o nome digitado.
6. O sistema salva a categoria na lista de categorias.

## Fluxo Alternativo
### FA01 - Cadastrando categoria desativada
1. No passo 4 do fluxo principal, o usuário confirma o cadastro da categoria com o nome de uma categoria desativada.
2. O sistema identifica que aquela categoria existe e está desativada.
3. O sistema pergunta ao usuário se ele deseja reativar aquela categoria.
4. O usuário confirma a reativação da categoria.
5. O sistema reativa a categoria e a disponibiliza novamente na lista de categorias.

### FA02 - Usuário cancela a reativação
1. No passo 4 do fluxo principal, o usuário confirma o cadastro da categoria com o nome de uma categoria desativada.
2. O sistema identifica que aquela categoria existe e está desativada.
3. O sistema pergunta ao usuário se ele deseja reativar aquela categoria.
4. O usuário cancela a reativação.
5. O sistema mantém a categoria desativada e retorna o usuário ao cadastro de categoria.

## Fluxo de Exceção
### FE01 - Campo vazio
1. No passo 4 do fluxo principal, o usuário confirma o cadastro da categoria sem informar o nome da categoria.
2. O sistema identifica que o campo não foi preenchido.
3. O sistema informa que o nome da categoria deve ser preenchido.
4. O sistema mantém o usuário no campo para informar o nome da categoria.

### FE02 - Nome de categoria existente
1. No passo 4 do fluxo principal, o usuário confirma o cadastro da categoria.
2. O sistema identifica que já existe uma categoria ativa com o nome informado.
3. O sistema informa que não é possível cadastrar uma categoria com um nome já utilizado por uma categoria ativa.
4. O sistema mantém o usuário no campo para informar o nome da categoria.

## Pós-condições
1. A categoria é cadastrada com sucesso.
2. A categoria fica disponível para ser utilizada na classificação de receitas e despesas.



