# ADR

Architectural Decision Records deste produto. Cada arquivo registra uma decisão que o código passa a obedecer.

## Quando escrever

Escreva um ADR quando a escolha nomear uma tecnologia, desenhar uma fronteira entre módulos ou fixar uma regra estrutural. Ajuste local que as práticas já cobrem dispensa ADR.

## Numeração

- O número tem quatro dígitos: `0001`, `0002`, `0003`.
- [`0000-template.md`](0000-template.md) é o modelo. Ele permanece neste repositório e nenhum ADR real usa o número `0000`.
- O próximo ADR usa o número seguinte ao maior já existente.
- Um número usado uma vez permanece. ADR substituído muda o status e aponta para o sucessor.

## Status

`proposto`, `aceito` ou `substituído por ADR NNNN`.

O agente trata como vigentes os ADRs `aceito`.
