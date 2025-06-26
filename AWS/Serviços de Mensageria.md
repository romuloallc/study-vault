---
id: Serviços de Mensageria
aliases: []
tags: []
Subject:
  - - AWS
Type: "[[Formação DevOps Professional]]  #aws  #linuxtips"
---
-  Amazon SQS
    -  Simple Queue Service
    -  Sistema distribuído de grande porte e volume
    - Modos:
        -  Standard
            -  Ordem das mensagens pode ser diferente
            -  Pode ocorrer mensagens duplicadas
        -  FIFO - First In/First Out
            -  Filas com garantia de ordem
    -  Producer/Consumer
    -  Visibility Timeout
        -  Tempo do consumer processar a mensagem
        -  Caso dê algum erro, a mensagem volta para a fila
    -  Dead-Letter Queue
        -  Fila de mensagens com erro, para que a mensagem não fique voltando

-  Amazon SNS
    -  Simple Notification Service
    -  Tópicos de mensagens
    -  Producer/Consumer
        -  Vários consumidores do tópico
    -  Assíncrono
    -  Modes:
        -  FIFO
        -  Standard
    -  Não possui DLQ
        -  Uma vez enviada, foi enviada 

-  Amazon MQ
    -  Serviços de mensageria normal
        -  Apache ActiveMQ
        -  RabbitMQ
    -  Provisiona uma instância para o serviço
    -  Não é serveless

-  Amazon Kinesis
    -  Produto de Streaming
        -  Parecido com o Kafka
