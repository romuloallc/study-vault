---
id: Performance Efficiency
aliases: []
tags: []
---

Subject: [[AWS]] 
Type: [[Formação DevOps Professional]]  #aws  #linuxtips 

---
-  Framework de arquitetura na AWS
    -  Relação do que é gasto pelo que é ganho
    -  Quando usar um serviço ao invés do outro?
    -  Selection:
        -  Compute:
            -  Instances
            -  Containers
            -  Functions
    -  Preço?
    -  Performance computacional - CPU, memória, storage, aceleração - GPU, FPGA
    -  Containers
        -  AWS Fargate - Unidade de processamento simples apenas para rodar o container
    -  Functions    
        -  AWS Lambda - Um código que irá responder a um evento
    -  [The USE Method](https://www.brendangregg.com/usemethod.html)
        -  "For every resource, check utilization, saturation, and errors."
            -  Resource: 
                -  All physical server functional components (CPU, disks, busses,...) 
            -  Utilization: 
                -  The average timie that the resource was busy servicing work
            -  Saturation: 
                -  The degree to which the resource has extra work which it can't service, often queued
            -  Errors:
                -  The count of error events
- [ ] 
