# Iniciar um produto

Roteiro desde o fork até o plano do MVP.

## 1. Ler a base

Leia, nesta ordem:

1. [`tecnologias.md`](../tecnologias.md)
2. [`produto/visao.md`](../produto/visao.md)
3. [`produto/identidade-visual.md`](../produto/identidade-visual.md)
4. [`produto/comportamento.md`](../produto/comportamento.md)
5. [`boas-praticas/`](../boas-praticas/)
6. ADRs com status aceito em [`adr/`](../adr/)

## 2. Pedir o que está vazio

Percorra os campos e separe os que ainda dizem `A preencher`.

Pergunte antes de seguir quando faltar algum destes:

- frontend ou backend em [`tecnologias.md`](../tecnologias.md)
- problema, quem usa ou resultado do MVP em [`produto/visao.md`](../produto/visao.md)

Pergunte também, no momento em que o plano for depender deles:

- banco de dados, quando o MVP persiste dado
- ferramentas de teste, quando o plano for citar como os testes rodam
- identidade visual, quando o plano incluir interface
- comportamento, quando o plano incluir fluxo, estado ou regra

Faça a pergunta com o nome do campo e o arquivo. Espere a resposta e grave no arquivo correspondente.

## 3. Entregar o plano do MVP

Com os campos obrigatórios preenchidos, siga [`skills/planejar-mvp.md`](../skills/planejar-mvp.md).

O resultado é um plano: fatias, riscos, testes e ADRs que ainda faltam. O código de aplicação começa quando esse plano estiver aceito.
