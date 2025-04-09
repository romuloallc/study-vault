Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Binário
	- Arquivos em formato HCL
	- Linguagem descritiva
	- Conecta na API e provisiona a infraestrutura
- State File - arquivo de estado
	- Gerado pelo Terraform
	- Usado para conferir o que tem e o que não tem provisionado
		- Se tiver provisionado e não tiver no código - Deleta
		- Se não tiver provisionado e tiver no código - Provisiona
		- Se tiver provisionado, mas diferente no código - Muda/Troca
	- Melhores práticas - Não guardar localmente, assim também ajuda ao compartilhamento para o time que está desenvolvendo

- Infraestrutura Mutável 
	- Aplicações ou máquinas que sofrem mudanças com o passar do tempo (Ex.: Servidor com Apache2 -> Nginx)
	- Conceito do floco de neve (Snowflake)
		- Cada floco de neve é único, não existe outro igual
		- Infra mutável tende a virar um floco de neve - Servidor ser único e não saber o que está nela, logo não poderá ser replicada

- Infra Imutável
	- Utilizar outra máquina para mudar a aplicação ou máquina e a antiga é descartada ou não utilizada mais
	- Assim, não tende a virar floco de neve
	- Terraform faz esse gerenciamento.