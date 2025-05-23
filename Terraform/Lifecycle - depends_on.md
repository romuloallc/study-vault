Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Meta Arguments
- Interferem no modo de como o Terraform funciona

- Lifecycle
	- Recurso com ciclo de vida  
		- create_before_destroy
			- Não é possível para recursos que demandam nomes únicos
		- prevent_destroy
		- ignore_changes
		- replace_triggered_by

- Depends_on
	- Garantir que um recurso depende do outro