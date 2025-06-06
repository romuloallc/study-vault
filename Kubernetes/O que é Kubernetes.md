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
        -  Portas:
            -  TCP 2378
            -  TCP 2380
        -  Guarda o estado do cluster
    -  Kube API Server
        -  Portas:
            -  TCP 6443
        -  "Cérebro" do cluster
        -  Toda a comunicação do cluster acontece através doKube API Server
    -  Kube Scheduler
        -  Portas:
            -  TCP 10251
        -  Responsável por saber onde os containers vão ser criados
        -  Gerenciamento dos containers/pods
    -  Kube Controller Manager
        -  Portas:
            -  TCP 10252
        -  Tem vários controllers
        -  Garante que o cluster está no estado desejado
        -  Gerenciador dos controllers
-  Workers
    -  Kubelet
        -  Portas:
            -  TCP 10250
        -  Agente do Kubernetes dentro do nó
        -  Passa as informações do nó para o Kube API Server
    -  Kube Proxy
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
