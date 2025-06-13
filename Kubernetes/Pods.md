---
id: Volumes
aliases: []
tags: []
---

Subject:
  - - Kubernetes
Type: "[[Formação DevOps Professional]]  #kubernetes #linuxtips"
---
# Volumes em Pods
-  Tipo:
    -  EmptyDir
        -  Definido no pod
        -  Pod reiniciou - volume continua
        -  Pod restartou (deletado e criado outro) - volume perdido
        -  Pod trocou de node - volume perdido
