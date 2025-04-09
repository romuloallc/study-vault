Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Mapeando o mundo real
	- Garante uma consistência do que se tem no código e no mundo real
- Metadata
- Performance
	- Terraform armazena cache de valores atribuidos a recursos no state
- Syncing
	- Remote State

```[bash]
terraform state
```

- Dá pra alterar o state direto, ou utilizar o pull/push
	- **Não é recomendado**
	- Utilizar apenas se for estritamente necessário