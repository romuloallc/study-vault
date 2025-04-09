Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---

- init
	- .terraform
		- diretório onde terá as informações que o binário Terraform precisa para executar
	- -upgrade
		- Atualizar o módulo e plugins
		- **É bom utilizar**
		- 
- plan
	- Executa o binário, verifica o código, verifica o state, mas não executa o código
	- Checagem mínima com as APIs
	- -out 
		- nome do plano
		- Salva em um arquivo o plano
	- -destroy
		- Plano de destruição dos recursos
- apply
	- Aplica o plano 
		- Se o plano for pra destruir o apply vai destruir a infraestrutura
	- Ex.: terraform apply "nome do plano"
	- Gera ou modifica o state file
- destroy
	- Destrói os recursos que estão no state file