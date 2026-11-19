# Contrato do agente

Este repositório começa como base de conhecimento. O código de aplicação entra no fork depois que a stack e o produto estão preenchidos e o plano do MVP foi aceito.

## Ordem de leitura

1. [`tecnologias.md`](tecnologias.md)
2. [`produto/visao.md`](produto/visao.md), [`produto/identidade-visual.md`](produto/identidade-visual.md) e [`produto/comportamento.md`](produto/comportamento.md)
3. [`boas-praticas/`](boas-praticas/) no trecho que a tarefa toca
4. [`adr/`](adr/) já aceitos
5. O playbook em [`skills/`](skills/) da tarefa atual
6. [`agentes/iniciar-produto.md`](agentes/iniciar-produto.md) quando o trabalho for começar o produto

## Regra de parada

Antes de propor código de aplicação, estes campos deixam de estar como `A preencher`:

- em [`tecnologias.md`](tecnologias.md): frontend e backend
- em [`produto/visao.md`](produto/visao.md): problema, quem usa e resultado do MVP

Com esses campos vazios, o agente lista o que falta e pede o conteúdo. Persistência espera o banco declarado em [`tecnologias.md`](tecnologias.md). Interface e fluxo esperam identidade visual e comportamento preenchidos.

## Onde registrar decisões

Uma escolha de tecnologia ou de estrutura concreta vira um ADR em [`adr/`](adr/). O ADR aponta para o que [`tecnologias.md`](tecnologias.md) declara. As práticas em [`boas-praticas/`](boas-praticas/) continuam agnósticas: framework, biblioteca e ferramenta moram na declaração de stack e nos ADRs.
