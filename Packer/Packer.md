---
id: Packer
aliases: []
tags: []
---

Subject: [[Packer]] 
Type: [[Formação DevOps Professional]]  #packer #linuxtips 

---
-  Hashicorp Nomad
    -  Criar uma imagem
    -  Exemplo:
        -  AMI da AWS
-  Fluxo comum:
    1. Packer utiliza o código
    2. Código chama o Ansible
    3. Ansible realiza as instalações necessárias
    4. Packer cria a imagem
    5. Terraform utiliza a imagem e provisiona uma EC2 com essa imagem criadak
-  Extensão: .pkr.hcl 
-  Obs.: ID da AMI muda por região
-  Bloco provisioner
    -  "ansible"

-  Como passar segredos pro Ansible
