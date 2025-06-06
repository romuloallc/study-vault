---
id: Intro
aliases: []
tags: []
---

Subject: [[Kubernetes]] 
Type: [[Formação DevOps Professional]]  #kubernetes #linuxtips 

----
# Pequeno Resumo
-  Container
    -  Isolamento de recursos
        -  CPU
        -  Memória
        -  Processos
        -  Usuários
    -  `cgroups`
    -  `namespaces`
-  Container Engine
    -  Responsável pela criação do container
    -  Não faz a comunicação com o Kernel do SO
        -  Container Runtime - responsável por se comunicar com o Kernel
-  Container Runtime
    -  Garantir que o container está em execução em isolamento
    -  Se comunica diretamente com o Kernel
    -  Vários tipos de runtime:
        -  containerd - Container Runtime do Docker - High Level
        -  runc - Low Level
        -  crun - Low Level 
-  Open Container Iniciative - OCI
    -  Consórcio de várias empresas
    -  Iniciativa criada para padronizar a criação de containers, runtimes e engines
    -  Desenvolveram o runtime runc


# Orquestração de Containers
-  Kubernetes
-  Hashicorp Nomad
-  Docker Swarm 
    -  Descontinuado
