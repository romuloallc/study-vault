---
id: Terraform - Notes
aliases: []
tags: []
---

Type: [[Terraform]] #terraform  

Notes and commands about my Terraform study

## Notes
#### Variables
- Variables can be assigned values in multiples ways:
	- Environment Variables
		- ```export TF_VAR_variablename="variablevalue"```
	- Command Line Flags 
	- From a File 
		- terraform.tfvars - default name for the file 
	- Variable Defaults
		- variables.tf - File for default values

##### Data types for Variables
- Restrict the type of value that will be accepted
	- If no type is set then any type is accepted

| Type Keywords |             Example             | Comment |
| ------------- |:-------------------------------:| ------- |
| string        |             "hello"             |         |
| list          | ["mumbai","singapore","brasil"] | First position = 0        |
| map           |   {name = "Rômulo", age = 25}   | Reference the key (name)        |
| number        |               525               |         |
| bool          |              true/false               |         |

#### Count Parameter
	- Count index starts with 0.
	- Count iterates resources
	- Count can iterate a list type variable 
---
## Commands
### Init
```bash
terraform init
```
---
### Plan
```bash
terraform plan
```
	
```bash
terraform plan -var="instancetype=t2.small"
```


	
```bash
terraform plan -var-file="custom.tfvars"
```




---
### Destroy
```bash
terraform destroy
```

```bash
terraform destroy -target aws_instance.myec2
```
---
