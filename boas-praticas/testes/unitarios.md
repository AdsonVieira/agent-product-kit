# Testes unitários

Um teste unitário protege uma regra ou um comportamento em memória, sem rede, disco, banco ou interface. As cinco letras de [FIRST](principios-first.md) se aplicam assim.

## Fast

A execução fica em memória. Colaboradores respondem no processo. Uma suíte unitária cabe no ciclo de editar e rodar.

## Isolated

O teste chama uma unidade e substitui os colaboradores por duplos que o próprio teste configura. A massa de um teste deixa de vazar para o próximo.

Um teste cobre um comportamento. O nome diz a condição e o resultado esperado.

## Repeatable

Relógio, identificador e aleatoriedade chegam por valores que o teste escolhe. O teste constrói os dados de que precisa e dispensa ordem global ou ambiente local.

## Self-validating

A asserção compara o resultado observável: valor devolvido, efeito pedido ao colaborador ou falha com motivo. A falha mostra o esperado e o obtido.

## Timely

O teste nasce com o comportamento, no mesmo intervalo em que a regra é escrita. A regra nova de [`produto/comportamento.md`](../../produto/comportamento.md) ganha um teste unitário que a descreve antes de a implementação se espalhar.

## O que fica nesta camada

Regra de domínio, transformação de valor e decisão pura. Travessia de banco, rede ou composição de módulos inteiros fica em [`integracao.md`](integracao.md).
