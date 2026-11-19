# Testes de integração

Um teste de integração protege uma fronteira: a entrega e o centro, ou o centro e a persistência. Um teste atravessa uma fronteira. As cinco letras de [FIRST](principios-first.md) se aplicam assim.

## Fast

A massa é a menor que ainda exercita o contrato. O teste sobe só o trecho da fronteira. Jornada completa de produto fica fora desta camada, repartida nas fronteiras que a compõem.

## Isolated

As outras fronteiras recebem duplos sob controle do teste. O banco, quando for a fronteira sob teste, começa num estado que o teste cria. Serviço externo à fronteira deixa de ser dependência viva.

## Repeatable

Cada teste prepara a massa e a recolhe ao terminar. Identidade e tempo vêm de valores fixados pelo teste. Duas execuções seguidas no mesmo ambiente produzem o mesmo veredito.

## Self-validating

A asserção olha o contrato observável da fronteira: resposta, efeito persistido ou motivo da recusa. A falha nomeia esse contrato. Passos internos da implementação ficam fora da asserção.

## Timely

O teste nasce quando a fronteira ganha contrato: formato da entrada, efeito guardado ou erro que atravessa a borda. O contrato escrito em [`tecnologias.md`](../../tecnologias.md) e a regra em [`produto/comportamento.md`](../../produto/comportamento.md) dizem o que afirmar.

## O que fica nesta camada

Uma chamada que entra pela borda e volta com o efeito do centro. Uma porta de persistência exercitada contra o banco declarado na stack. Regra pura continua em [`unitarios.md`](unitarios.md). Direção de dependência entre módulos continua em [`arquitetura.md`](arquitetura.md).
