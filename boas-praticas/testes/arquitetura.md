# Testes de arquitetura

Um teste de arquitetura protege uma regra estrutural do repositório: quem pode depender de quem, que módulo existe, que ciclo é proibido. Ele olha a estrutura, e um cenário de uso fica nas outras camadas. As cinco letras de [FIRST](principios-first.md) se aplicam assim.

## Fast

A verificação lê o código ou o grafo de módulos no processo, sem rede e sem banco. A suíte de arquitetura acompanha a suíte unitária no fluxo de mudança.

## Isolated

Cada teste protege uma regra. A massa é a árvore de código, e o teste dispensa dado de produto, usuário ou fixture de jornada.

## Repeatable

O mesmo commit produz o mesmo veredito. A regra está escrita no teste, com a lista do que é permitido e do que é proibido. Ambiente local deixa de influenciar o resultado.

## Self-validating

A falha nomeia a regra violada e o ponto da violação: o módulo, a dependência ou o ciclo. Quem lê o resultado sabe o que corrigir sem reinspecionar o repositório à mão.

## Timely

O teste nasce com o ADR que cria a regra. Enquanto o ADR está proposto, o teste pode nascer junto, descrevendo a estrutura aceita. ADR aceito e teste correspondente andam no mesmo conjunto de mudanças. ADR substituído atualiza ou aposenta o teste no mesmo momento.

## O que esta camada protege

Direção das dependências descrita em [`boas-praticas/backend/principios.md`](../backend/principios.md). Fronteiras nomeadas num ADR. Ausência de ciclo entre os módulos que o ADR separou.

Comportamento de uma regra continua em [`unitarios.md`](unitarios.md). Contrato de uma fronteira em execução continua em [`integracao.md`](integracao.md). A ferramenta que percorre as dependências fica em Ferramentas de teste, em [`tecnologias.md`](../../tecnologias.md).
