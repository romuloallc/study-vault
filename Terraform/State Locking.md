Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Garantir que o state não mude enquanto você estiver mudando
	- Modifica o código
	- Lock state
	- Atualiza o state
	- Unlock state
- Para garantir o State Locking:
	- (AWS) Utilize o dynamodb_table no provider
		- Criar a parte, um dynamodb_table
- Quando o State está travado não é possível rodar plan/apply/destroy
	- Mas dá para realizar o bypass: -lock=false
		- Utilize somente com ```terraform plan```, nunca para *apply*
- Como o dynamodb_table foi criado de maneira apartada
	- É possível que seja apagado durante a execução de algum comando de apply/destroy
		- E após o termino do comando o Terraform não consegue destravar o state
			- Solução: 
				- 1 - Remover a pasta **.terraform** para garantir que está sem cache
				- 2 - Remover a linha do dynamodb_table do provider