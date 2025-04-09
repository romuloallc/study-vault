Subject: [[Terraform]] 
Type: [[Formação DevOps Professional]]  #terraform #linuxtips

---
- Empresa que vende recursos, serviços e aplicações
- A grande diferença das grandes Clouds é a API
	- A API se comunica com os serviços
	- O usuário se comunica com a API
	- E recursos, como Terraform, se comunica com a API
- Organização dos Serviços
	- Regiões - regiões geográficas
		- Zonas - áreas dentro das regiões
- O arquivo de State do Terraform não deve ser armazenado localmente
	- Normalmente é utilizado o serviço de armazenamento de objetos das Clouds
		- AWS - S3
		- GCP - Cloud Storage
- IAM
	- Quem pode fazer o que em quais recursos
	- Who can do What on Which resources
	- Criar usuário ou Service Account para o Terraform utilizar para se comunicar com a API 