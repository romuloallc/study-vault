---
id: Desempenho no EC2 e EBS
aliases: []
tags: []
---

Subject: [[AWS]] 
Type: [[Formação DevOps Professional]]  #aws  #linuxtips 

---
-  Composição de uma instância EC2
    -  CPU
    -  Memória
    -  Instance Storage
    -  Placa de aceleração
    -  Interface de Rede
-  Instance Start-Stop
    -  Pode passar muito tempo depois de uma parada
    -  Instance Storage é efêmero ao reiniciar a máquina são perdidos
        -  Local device
        -  Efêmero
        -  Capacidade fixa
        -  Custo incluído no tipo da instância
    -  EBS Volumes
        -  Remote Service
        -  Durável
        -  Capacidade configurável
        -  Custo separado
        -  Algumas famílias tem instâncias EBS Optimized
            -  Essas tem 2 interfaces de rede
                -  Uma para tráfego normal e outra para o volume EBS
                -  Sem concorrência de tráfego
        -  É possível conectar o Volume EBS a mais instâncias - Multi Attach
            -  Observar a escrita concorrente para não ter erros


-  Snapshot no EBS
    -  Snapshot - Uma cópia no instante de tempo armazenados no S3
        -  São graduais - Snapshots novos referênciam os antigos
    -  Regras de ciclo de vida
        -  Apagar Snapshots antigos
            -  Contagem
            -  Período
    -  É possível criar imagens - AMI - a partir dos snapshots
    -  Consistência
        -  Parar a instância antes de tirar o Snapshot 
        -  Flush na memória

