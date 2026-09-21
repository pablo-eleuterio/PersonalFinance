# UC15 - Reservar Valor para Meta

## Objetivo
Permitir que o usuário reserve um determinado valor para uma meta financeira.

## Ator Principal
Usuário.

## Pré-condições
1. O usuário deve estar logado no sistema.
2. O usuário deve ter ao menos uma meta cadastrada no sistema.

## Gatilho
O usuário acessa a opção de reservar valor para a meta.

## Fluxo Principal
1. O usuário acessa a opção de reservar para a meta.
2. O sistema solicita o valor a ser reservado e a conta financeira de onde sairá o valor.
3. O usuário informa o valor e seleciona a conta financeira.
4. O usuário confirma a reserva.
5. O sistema valida as informações.
6. O sistema registra o valor reservado, vinculando-o à meta e à conta financeira selecionada.
7. O sistema desconta o valor do saldo disponível da conta financeira selecionada.
8. O sistema atualiza o saldo consolidado disponível e o progresso da meta.

## Fluxo de Exceção
### FE01 - Saldo insuficiente
1. No passo 4 do fluxo principal, o usuário confirma a reserva.
2. O sistema identifica que o usuário não possui saldo suficiente na conta financeira informada.
3. O sistema informa que o saldo daquela conta é insuficiente.
4. O sistema mantém o usuário no formulário para corrigir as informações.

### FE02 - Valor inválido
1. No passo 4 do fluxo principal, o usuário confirma a reserva com o valor menor ou igual a 0.
2. O sistema identifica que o valor informado para a reserva é inválido.
3. O sistema informa que o valor a ser reservado deve ser maior que 0.
4. O sistema mantém o usuário no formulário para corrigir as informações.

## Pós-condições
1. O sistema reserva o valor para a meta com sucesso.
2. O valor é descontado da conta financeira selecionada.
3. O saldo consolidado do usuário é atualizado.
