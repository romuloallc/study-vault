---
id: Nomad
aliases: []
tags: []
---

Subject: [[Nomad]] 
Type: [[Formação DevOps Professional]]  #nomad #linuxtips 

----
-  Alternativa ao Kubernetes
-  Gerencia aplicações em containers e aplicações sem container 
-  Integrações nativas com os outros produtos Hashicorp:
    -  Terraform
    -  Consul 
    -  Vault
-  Servers - Clients
-  Portas:
    -  Precisa de 3 portas nos Servers e 2 nos Clients
    -  TCP, UDP, or both
        -  HTTP API - 4646
        -  RPC - 4647 - TCP only
        -  Serf WAN - 4648
    -  Portas dinâmicas: 20000 - 32000
