Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Informações sobre a infraestrutura disponível na linha de comando
- Output values são similar a return values de liguagens de programação
	- Saída do comando
- Pode ser usado
	- Um recurso expões uma série de informações a um outro recurso
	- Mostra certos valores na CLI após o **apply**
	- Quando o remote state é utilizado, os valores de output podem ser acessados via ```terraform remote state data_source```

- Utilizar o terraform remote state não é recomendado, somente em casos estritamente necessários