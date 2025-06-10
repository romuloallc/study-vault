---
id: Intro
aliases: []
tags: []
---

Subject: [[Kubernetes]] 
Type: [[Formação DevOps Professional]]  #kubernetes #linuxtips 

----
# O que é?
-  Orquestrador de containers

## Arquitetura
-  Nodes
    -  Control Plane
        -  Serviços para controlar o cluster
        -  Responsável pela saúde, disponibilidade, capacidade e armazenar o estado do cluster
    -  Workers
        -  Onde esta rodando as aplicações do cluster
    -  É possivel rodar aplicações no control plane, mas não é recomendado e não é possível por default

### Componentes
-  Control Plane
    -  `etcd`
        -  Guarda o estado do cluster
        -  Datastore chave-valor
            -  Kubernetes utiliza para armazenar as especificações, status e configurações do cluster
        -  Dados armazenados no `etcd` são manipulados apenas atráveis da API
        -  Apenas executado em nodes com role Control Plane
            -  É possível executar em clusters externos, específicos para esse propósito
        -  Portas:
            -  TCP 2379
            -  TCP 2380
    -  Kube API Server
        -  "Cérebro" do cluster
        -  Toda a comunicação do cluster acontece através do Kube API Server
        -  JSON sobre HTTP
        -  Comunicação entre componenetes são estabelecidas através de requisições REST
        -  Portas:
            -  TCP 6443
    -  Kube Scheduler
        -  Responsável por saber em qual node o pod/container será hospedado
        -  Gerenciamento dos containers/pods
        -  Seleção dos nodes se baseia na quantidade de recurso dos nodes e também estados dos nodes
            -  Para garantir uma boa distribuição 
        -  Também é possível definir políticas, afinidade e etc...
        -  Portas:
            -  TCP 10251
    -  Kube Controller Manager
        -  Tem vários controllers
        -  Garante que o cluster está no estado definido pelo `etcd`
        -  Gerenciador dos controllers
        -  Portas:
            -  TCP 10252
-  Workers
    -  Kubelet
        -  Agente do Kubernetes dentro do nó
            -  Gerencia os pods dentro do workers
                -  Inicia, para e mantém os containers e os pods em funcionamento desejado pelo controller
        -  Passa as informações do nó para o Kube API Server
        -  Portas:
            -  TCP 10250
    -  Kube Proxy
        -  Atua como Proxy e Load Balancer
        -  Efetua roteamento de requisições para os pods corretos
        -  Gerencia a parte de rede do nó
        -  Faz a comunicação dos pods com o resto do mundo
    -  NodePort
        -  Tipo de serviço
        -  Porta da aplicação <-> Porta do nó
        -  Portas:
            -  TCP 30000 - 32767
    -  WeaveNet
        - Portas:
            -  TCP/UDP 6783
            -  TCP/UDP 67884
