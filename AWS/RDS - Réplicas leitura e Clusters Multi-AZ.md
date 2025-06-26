---
id: RDS - Réplicas leitura e Clusters Multi-AZ
aliases: []
tags: []
---

Subject: [[AWS]] 
Type: [[Formação DevOps Professional]]  #aws  #linuxtips 

---
-  Cluster Multi-AZ
    -  1 réplica de escrita
    -  2 réplicas de leitura
        -  Réplicas tem transações assíncronas
        -  Delay de replicação para as réplicas de read only
        -  Replica lagging
-  As vezes ter uma réplica temporária para fazer operações sem impactar
    -  Relatório
    -  Cópia
