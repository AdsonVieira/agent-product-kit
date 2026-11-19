# Kit para novos produtos

Base de Markdown para começar um produto. O repositório guarda o que o agente precisa ler antes de planejar o MVP: stack, definição de produto, práticas, skills e decisões de arquitetura.

Cada produto novo nasce de um fork ou de um clone. As práticas permanecem. A stack, os documentos de produto e os ADRs seguintes são deste produto.

## Como começar

1. Faça um fork ou um clone deste repositório.
2. Preencha [`tecnologias.md`](tecnologias.md).
3. Preencha [`produto/visao.md`](produto/visao.md), [`produto/identidade-visual.md`](produto/identidade-visual.md) e [`produto/comportamento.md`](produto/comportamento.md).
4. Peça ao agente para seguir [`agentes/iniciar-produto.md`](agentes/iniciar-produto.md) e entregar o plano do MVP.
5. Registre em [`adr/`](adr/) cada decisão de tecnologia ou de estrutura.

Um campo que ainda contém `A preencher` está vazio. O agente pede o conteúdo desse campo antes de propor código de aplicação.

## Mapa

| Pasta | Função |
| --- | --- |
| [`tecnologias.md`](tecnologias.md) | Stack deste produto. Único lugar que nomeia frameworks e ferramentas. |
| [`agentes/`](agentes/) | Roteiros de operação do agente. |
| [`skills/`](skills/) | Playbooks de uma tarefa: stack, produto, ADR e plano do MVP. |
| [`produto/`](produto/) | Visão, identidade visual e comportamento. |
| [`adr/`](adr/) | Decisões de arquitetura, numeradas. |
| [`boas-praticas/`](boas-praticas/) | Código, frontend, backend e testes, sem amarrar tecnologia. |

[`AGENTS.md`](AGENTS.md) define a ordem de leitura e a regra de parada.
