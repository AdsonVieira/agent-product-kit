# Clean code

Código que outra pessoa entende no ponto em que precisa mudar. As práticas abaixo descrevem o que observar e o que preferir. A stack concreta está em [`tecnologias.md`](../../tecnologias.md).

## Nomes

Observe um nome que exige abrir o corpo para saber o efeito.

Prefira um nome com o efeito no vocabulário do produto: o papel, a regra ou o resultado. Unidade, limite e condição entram no nome quando mudam o significado.

## Tamanho e nível

Observe uma função que mistura política do domínio com detalhe de transporte, formato ou persistência.

Prefira uma função com uma responsabilidade no mesmo nível de abstração. O nível de cima chama operações nomeadas. O detalhe mora na operação de baixo.

## Um lugar para cada regra

Observe a mesma regra repetida em dois pontos que podem divergir.

Prefira a regra num único lugar, com um nome. Quem precisa dela chama esse lugar.

## Comentários

Observe um comentário que repete o que o nome já diz.

Prefira um comentário que registre a restrição, a origem da regra ou a consequência de mudar aquilo. O nome continua responsável pelo que o código faz.

## Erros visíveis

Observe uma falha engolida, convertida em valor vazio ou registrada sem quem chama saber.

Prefira um resultado que quem chama trata: valor produzido ou falha com motivo. O motivo diz o que faltou ou o que foi recusado.

## Forma

Observe um arquivo que inventa um arranjo diferente do vizinho sem uma decisão registrada.

Prefira a forma já usada no módulo. Uma forma nova pede um ADR quando passa a valer para o resto do código.

## Parâmetros

Observe uma lista que carrega dados soltos cujo sentido só aparece dentro da função.

Prefira parâmetros que cabem na leitura da assinatura. Dados que andam juntos formam um tipo com nome do conceito.
