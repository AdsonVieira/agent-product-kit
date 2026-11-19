# Planejar o MVP

Use depois que a regra de parada de [`AGENTS.md`](../AGENTS.md) estiver satisfeita.

1. Leia a visão, o comportamento, a stack, as práticas que as fatias tocam e os ADRs aceitos.
2. Recorte o resultado do MVP em fatias que cabem numa entrega. Cada fatia tem um comportamento observável.
3. Para cada fatia, diga qual prática de [`boas-praticas/testes/`](../boas-praticas/testes/) se aplica e em qual camada o teste nasce: unitário, integração ou arquitetura.
4. Liste riscos e os ADRs que ainda faltam para a estrutura ficar explícita.
5. Aponte campos `A preencher` que a fatia usa, para que o plano espere esse conteúdo.
6. Entregue o plano e espere o aceite antes de escrever código de aplicação.

O plano cita a stack pelo que [`tecnologias.md`](../tecnologias.md) declara. As práticas entram pelo comportamento que exigem, com o nome do arquivo.
