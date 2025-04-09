Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- valores -> são tipos de expressions
- Types
	- string
		- Entre aspas
		- Texto
	- number
		- Número sem aspas
	- bool
		- true
		- false
		- Sem aspas
	- list
		- Valores dentro de  \[ ]
	- set
		- Coleção de valores únicos sem ordenação
	- map
		- Lista de chave = "valor"
		- Entre { }
	- null
		- Valor especial
		- Representa falta ou omissão de valor
		- Bastante utilizado em condicionais
- Terraform converte alguns valores para *string* se necessário, quando ele já sabe que o valor naquele lugar é uma string
	- Mas sempre se atente ao tipo da expression