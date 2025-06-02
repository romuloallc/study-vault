---
id: Docker Compose
aliases: []
tags: []
---

Subject
Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips 

----
-  Exclusivo para plataform Docker
-  Não utilizar em produção, apenas em laboratórios locais e testes
-  Forma de passar para o Docker parâmetros para subir vários containers
-  Os container utilizados pelo Docker Compose são **removidos**
-  Utilizando Volumes no Compose, esse cria o volume com um `compose_<nomedovolume>`. É possível desabilitar
-  Docker Compose consegue buildar imagens - utilize o `build`
-  `--scale <number>` Alterar o número de réplicas
-  Limitar recursos no Docker Compose:
    -  limit
        -  Define o máximo de recursos que o Compose pode utilizar 
    -  Reserva
        -  Garante o container tenha uma quantidade mínima de recursos
-  Algumas opções:
```[yaml]
version
services
    <nomedoservice>:    
        build: 
            context:  <contextodoDockerfile>
            dockerfile: <nomedoDockerfile>
        container_name: <nomedocontainer>
        env_file:
            - .env
        volumes:
            - type: <tipodovolume>
              source: <origemdovolume>
              target: /<diretóriodovolumenocontainer>
        deploy:
            replicas: <númerodereplicas>
            labels: 
                - <label>
            update_config:
                parallelism: 2
                delay: 10s
            restart_policy: 
                condition: on-failure
                delay: 5s
                max_attempts: 3
```
