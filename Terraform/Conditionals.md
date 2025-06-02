Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Expressions
	- Valores computados em uma configuração
		- "hello"
		- 5
	- Operators
		- Order
			```!, - (multiplication by -1)```
			```*, /, %```
			```+. - (subtraction)```
			```>, >=, <, <=```
			```==, !=```
			```&& (AND)```
			```|| (OR)```
		- Arithmetics Operators 
			- `a+b`
			- `a-b`
			- `a*b`
			- `a/b`
			- `a%b`
			- `-a`
		- Equality Operators
			- `a == b`
			- `a != b`
		- Comparison Operators
			- `a < b`
			- `a <= b`
			- `a > b`
			- `a >= b`
		- Logical Operators
			- `a || b`
			- `a && b`
			- `!a`
	- Conditional Expressions
		- `condition ? true_val : false_val`
			-  `environment == "production" ? 2 : 1`