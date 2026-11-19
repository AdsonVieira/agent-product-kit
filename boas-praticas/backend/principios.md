# Princípios de backend

O comportamento do produto mora no centro. Entrega e persistência ficam nas bordas e apontam para esse centro. O framework e o banco deste produto estão em [`tecnologias.md`](../../tecnologias.md).

## Bordas e centro

A borda recebe a chamada, traduz para o vocabulário do domínio e devolve a resposta no formato da API declarada.

O centro aplica as regras de [`produto/comportamento.md`](../../produto/comportamento.md) sobre tipos já válidos.

A persistência entra por uma porta nomeada pelo que o domínio precisa guardar ou buscar. A implementação dessa porta conhece o banco. O centro conhece a porta.

## Dependências para dentro

A dependência segue para o centro: a borda importa o centro, e o centro importa tipos do centro. Mecanismo de entrega, cliente de rede e mecanismo de persistência permanecem na borda.

Observe uma regra de negócio que só existe dentro do adaptador de entrada ou da consulta ao banco. Prefira a regra no centro, com a borda apenas traduzindo.

## Validação na borda

A entrada é validada na borda, antes da regra. Validação confirma presença, formato e faixa. A regra do domínio confirma o que é permitido no estado atual do produto.

Valor que atravessa a borda chega ao centro já checado no formato. O centro recusa o que fere a regra e devolve o motivo.

## Erro explícito

Cada falha que quem chama precisa tratar tem um resultado explícito e um motivo: dado inválido, regra recusada, recurso ausente ou dependência indisponível.

Observe uma falha convertida em sucesso vazio, ou um erro genérico que esconde o motivo. Prefira o motivo específico no ponto em que a falha nasce.

Falha inesperada sobe com o contexto da operação. A borda traduz esse contexto na resposta, sem engolir a causa.

## Consulta e comando

Consulta devolve dado e preserva o estado.

Comando muda estado e descreve o efeito produzido.

Observe uma operação que ao mesmo tempo calcula uma leitura e grava um efeito. Prefira separar, para o leitor saber se repetir a chamada muda alguma coisa.

## Repetir a operação

Uma operação que a rede pode entregar duas vezes declara o que a segunda execução faz. Quando o efeito precisa ocorrer uma vez, a segunda chamada devolve o resultado da primeira. Quando o efeito pode se acumular, o contrato diz isso em [`produto/comportamento.md`](../../produto/comportamento.md).
