Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips

----
- Filesystem do container -> Volátil
	- Informação escrita nele é perdida quando o container morre
- Mapear um diretório dentro do container
- Diretório normalmente vem do host
- Tipos:
	- Bind
		- Aponta um diretório do host dentro do diretório do container
		- Tudo que mudar dentro do diretório, muda dentro do container
		- Tudo que mudar dentro do container, muda dentro do diretório
		- Como se fosse um NFS
	- Volume
		- Mais recomendado
		- Docker gerencia os Volumes
		- Diretório dentro do host -> pro Container, mas o Docker gerencia dentro dos Docker Volumes
		- /var/lib/docker/volumes/
	- TMPFS
		- Dados guardados na memória
		- Dados temporários
		- Usado em casos muito específicos
- Volumes continuar a existir mesmo se o container for deletado
