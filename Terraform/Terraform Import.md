Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Pega  informações da máquina que foi provisionada fora do Terraform e coloca no State

```[bash]
terraform import [options] [terraform address] [resource id]
```

- Novo modo de importar
	- Bloco **import**
- Generated Resources
	- Forma experimental
	- Gera o arquivo .tf do recurso com **todas** as informações