---
id: Funções e Arquiteturas Orientadas a eventos
aliases: []
tags: []
Subject:
  - - AWS
Type: "[[Formação DevOps Professional]]  #aws  #linuxtips"
---
-  AWS Lambda
    -  Execução de funções a partir de eventos sem provisionamento de servidores
    -  Serveless
    -  Pode ser um pacote ou um container para ser executado
    -  Executa apenas por demanda
-  AWS Fargate
    -  Mesma ideia do Lambda, mas focado em container
-  Amazon EventBridge
    -  Fluxo de mensagens para compor as aplicações serveless
-  Amazon SQS
    -  Serviço de mensagens
    -  Armazena e entrega para outras aplicações
-  SNS
    -  Mensagens por "assinantes"
    -  Topic - Subscribers
    -  Tipo o "Pub-Sub"
-  Amazon API Gateway
    -  Recebe solicitações HTTP
    -  Mapeia requisições para lambda ou outros serviços
    -  Pode ser feito cache e segurança
