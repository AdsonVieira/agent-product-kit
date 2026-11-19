# FIRST

FIRST é o critério de desenho de um teste, nas três camadas: unitário, integração e arquitetura. Cada camada aplica as cinco letras do seu jeito, nos arquivos [`unitarios.md`](unitarios.md), [`integracao.md`](integracao.md) e [`arquitetura.md`](arquitetura.md).

## Fast

O teste termina rápido o bastante para rodar no fluxo de mudança. O custo alto pede um recorte menor: menos dados, menos fronteiras, menos ambiente.

## Isolated

O teste exerce um comportamento e controla o que está ao redor. Outro teste deixa de ser pré-condição. A ordem da suíte deixa de alterar o resultado.

## Repeatable

A mesma árvore de código e a mesma massa produzem o mesmo resultado. Relógio, aleatoriedade e resíduo de execução anterior entram sob controle do teste.

## Self-validating

O teste decide sozinho se passou. A falha nomeia o comportamento ou a regra que quebrou. A leitura do log dispensa interpretação manual.

## Timely

O teste nasce junto da decisão que ele protege: com o comportamento, com a fronteira ou com o ADR. O teste atrasado descreve o que o código já fez por acaso.
