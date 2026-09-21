# UC24 – Gerenciar Perfil

## Objetivo
Permitir que o usuário visualize seus dados e altere seu nome.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.

## Gatilho
O usuário acessa seu perfil.

## Fluxo Principal
1. O usuário acessa seu perfil.
2. O sistema exibe os dados do perfil.
3. O usuário seleciona a opção de editar o nome.
4. O sistema disponibiliza o campo de nome para edição.
5. O usuário altera o nome.
6. O usuário salva a alteração.
7. O sistema atualiza o nome do usuário.

## Fluxo de Exceção
### FE01 - Nome inválido
1. O sistema identifica que o nome informado é inválido.
2. O sistema informa ao usuário que o nome deve ser preenchido corretamente.
3. O usuário informa um novo nome.
4. O fluxo retorna ao passo 6 do Fluxo Principal.

## Pós-condições
1. O nome do usuário é atualizado no sistema.
2. Os demais dados do perfil permanecem inalterados.