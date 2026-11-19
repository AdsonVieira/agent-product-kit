# Princípios de frontend

A interface mostra o estado que recebeu e devolve a intenção de quem usa. A biblioteca que desenha essa interface está em [`tecnologias.md`](../../tecnologias.md). As regras abaixo valem para a escolha que estiver declarada lá.

## Limite da interface

Uma parte de apresentação recebe dados prontos e devolve intenções: o que a pessoa pediu, com os valores que ela informou.

Uma parte de coordenação obtém os dados, guarda o estado da jornada e traduz falha em estado de erro.

Observe uma parte que ao mesmo tempo desenha, busca dado e decide regra de negócio. Prefira separar o desenho da coordenação, e deixar a regra onde [`boas-praticas/backend/principios.md`](../backend/principios.md) a coloca. A interface que precisa da regra chama o resultado dela.

## Dono do estado

Cada dado que a tela mostra tem um dono. O dono atualiza esse dado. As outras partes leem.

Observe o mesmo dado gravado em dois lugares que podem divergir. Prefira uma origem e derive o resto na leitura.

Estado de jornada da tela fica na coordenação daquela jornada. Estado que sobrevive à jornada fica na borda correspondente: sessão, rascunho ou servidor, conforme o comportamento do produto.

## Estados que a pessoa vê

Vazio, carregando, erro e sucesso são estados desenhados, com conteúdo próprio.

- Vazio explica o que ainda não existe e qual ação começa.
- Carregando ocupa o lugar do conteúdo que vai chegar e preserva o que já estava na tela.
- Erro diz o que falhou e qual caminho existe a seguir: tentar de novo, corrigir um campo ou voltar.
- Sucesso confirma o efeito que a pessoa pediu.

O texto desses estados segue o tom de [`produto/identidade-visual.md`](../../produto/identidade-visual.md) e os fluxos de [`produto/comportamento.md`](../../produto/comportamento.md).

## Acessibilidade

Cada controle tem nome que a tecnologia assistiva lê. A ordem de tabulação segue a ordem da tarefa. O foco fica visível. A ação principal também funciona por teclado.

Cor carrega contraste suficiente entre texto e superfície. Cor acompanha texto ou ícone quando indica erro, sucesso ou obrigatoriedade.

O campo com erro aponta para a mensagem que explica a correção.

## Efeitos na borda

Rede, relógio, armazenamento local e inscrição em eventos ficam na borda da interface. A parte de apresentação recebe o resultado e devolve a intenção.

Observe um desenho que dispara efeito ao ser calculado. Prefira o efeito na coordenação, disparado pela intenção ou pela entrada na jornada.
