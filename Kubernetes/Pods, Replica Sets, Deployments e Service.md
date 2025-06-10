---
id: Pods, Replica Sets, Deployments e Service
aliases: []
tags: []
---

Subject: [[Kubernetes]] 
Type: [[Formação DevOps Professional]]  #kubernetes #linuxtips 

----
-  Pods
    -  Menor instância/unidade do Kubernetes
    -  Pod contém um ou mais container
        -  Caso tenha mais de um container no pod ocorre -> compartilhamento de isolamento
    -   

-  Deployment
    -  Características das réplicas/Ciclo de vida da aplicação
        -  Imagem
        -  Limites
        -  Portas
        -  Volumes
        -  Variáveis de ambiente

-  Replica Set
    -  É criado pelo Deployment
    -  Responsável por garantir que o número de réplicas seja igual ao número desejado

-  Service
    -  Forma de expor o Deployment para outros serviços ou usuários
    -  Vários tipos de Service
        -  Load Balancer
        -  Node Port
        -  ClusterIP
    -  Como um load balancer
