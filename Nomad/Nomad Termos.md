---
id: Nomad Termos
aliases: []
tags: []
---

Subject: [[Nomad]] 
Type: [[Formação DevOps Professional]]  #nomad #linuxtips 

----
### Server:
-  Gerenciar o cluster
-  3 ou 5
    -  Garante redundância e diminui pontos de falhas
-  Analogia ao Kubernetes: Como se fosse o Control Plane
-  Comunicação entre servers via GOSSIP Protocol - TCP/UDP 4648 
-  Comunicação entre servers e clients - RPC - TCP 4647
-  Server Leader e Serves Followers

### Task
-  Menor unidade do cluster Nomad 

### Task Group
-  Conjunto de `tasks`
-  `Tasks` que precisam ser executadas juntas - no mesmo Client/node

### Client
-  Vão receber containers/aplicações
-  Analogia ao Kubernetes: Como se fosse os Workers
-  Comunicação com os servers via RPC - TCP 4647

### Driver 
-  Executa as `tasks`, cada `task` vai utilizar um Driver diferente:
    -  Docker -> Executa containers
    -  Java   -> Executa a aplicação
    -  QEMU   -> Executa VMs

### Job
-  Analogia ao Kubernetes: Como se fosse o deployment
-  Definine detalhes do deploy
-  Composto por um ou mais `task groups`
