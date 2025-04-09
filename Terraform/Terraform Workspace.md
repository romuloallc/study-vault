Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Segregação de ambientes "virtualizados"
	- Workspace padrão: default
	- Mantém o mesmo provider
	- Pode ser utilizado para ambientes descartáveis
		- Não vale a pena, mas é possível
	- Manipulação do state fica mais complicada
- Tem formas melhores de trabalhar com ambientes segregados 

```[bash]
terraform workspace new [nome-workspace]
```