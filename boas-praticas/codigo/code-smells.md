# Code smells

Um smell é um sinal de leitura: a estrutura atual dificulta a próxima mudança. Abaixo, o que observar e o que preferir no lugar. Confirme o smell no código antes de reorganizar.

## Método longo

Observe um bloco em que o nome promete um efeito e o corpo executa várias etapas de naturezas diferentes.

Prefira extrair cada etapa para uma operação nomeada pelo efeito dela.

## Módulo grande

Observe um arquivo que acumula regras de momentos diferentes do produto.

Prefira separar pelo motivo de mudança. O que muda junto permanece junto.

## Obsessão por primitivo

Observe texto, número ou lista carregando uma regra que se repete em cada uso: formato, faixa, unidade ou invariante.

Prefira um tipo com essa regra dentro. Quem recebe o tipo já recebe um valor válido.

## Inveja de dados

Observe uma operação que lê o detalhe interno de outro módulo para decidir.

Prefira mover o comportamento para o módulo que já possui os dados.

## Cirurgia de espingarda

Observe uma mudança de produto que exige editar vários módulos para uma única regra.

Prefira reunir essa regra num módulo e deixar os outros chamarem.

## Mudança divergente

Observe um módulo editado por motivos que não têm relação entre si.

Prefira um módulo por motivo de mudança.

## Código morto

Observe caminho, parâmetro ou abstração que nenhuma chamada usa.

Prefira apagar. O histórico do repositório guarda a versão anterior.

## Generalidade especulativa

Observe interface, camada ou configuração criada para um caso que o produto ainda não tem.

Prefira a abstração no segundo uso real, quando as duas variações já existem.

## Número mágico

Observe um literal cujo motivo não está no ponto de uso.

Prefira uma constante nomeada pela regra que o valor representa.

## Flag que esconde dois comportamentos

Observe um booleano que escolhe, dentro da mesma operação, dois fluxos com efeitos diferentes.

Prefira duas operações nomeadas, cada uma com o seu efeito.

## Acoplamento temporal oculto

Observe chamadas que só funcionam numa ordem que a assinatura deixa de dizer.

Prefira uma operação que executa os passos na ordem certa, ou um tipo que só existe depois do passo anterior.
