Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Cada módulo ter seu próprio repositório
	- Repositório - Módulo: EC2
		- Examples
		- Tests
	- No repositório do Projeto - Produto
		- Copia os arquivos: main.tf - provider.tf
		- Mais avançado: Reusable workflows
			- Reutiliza uma mesma pipeline

- É comum utilizar um único Storage com pastas separadas para armazenar os buckets

- Não utilizar Workspaces - Própria Terraform não recomenda

- Organização de pastas de Terraform
	- iac/terraform
		- dev
			- main.tf
			- provider.tf
		- prod
			- main.tf
			- provider.tf

- Cloudtrail
	- Event history - Ver os erros e logs