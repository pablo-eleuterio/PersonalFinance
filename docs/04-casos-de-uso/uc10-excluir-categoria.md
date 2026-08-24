# UC10 - Excluir Categoria

## Objetivo
Permitir que o usuário exclua uma categoria existente.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve ter ao menos uma categoria cadastrada.

## Gatilho
O usuário acessa a opção de excluir categoria.

## Fluxo Principal
1. O usuário acessa a opção de excluir categoria.
2. O sistema solicita a confirmação da exclusão da categoria.
3. O usuário confirma a exclusão.
4. O sistema verifica os vínculos da categoria.
5. O sistema identifica que a categoria não possui vínculos com receitas ou despesas.
6. O sistema exclui a categoria.

## Fluxo Alternativo
### FA01 - Categoria vinculada a receitas ou despesas
1. No passo 4 do fluxo principal, o sistema identifica que a categoria possui vínculos com receitas ou despesas.
2. O sistema desativa a categoria.
3. O sistema remove a categoria das opções disponíveis para novos lançamentos.
4. A categoria permanece vinculada às receitas e despesas já existentes.

### FA02 - Usuário cancela a exclusão
1. No passo 3 do fluxo principal, o usuário cancela a exclusão.
2. O sistema retorna o usuário à lista de categorias.
3. Nenhuma alteração é realizada na categoria.

## Pós-condições
1. Caso a categoria não possua movimentações vinculadas, ela é excluída com sucesso.
2. Caso a categoria possua movimentações vinculadas, ela é desativada e deixa de estar disponível para novos lançamentos.