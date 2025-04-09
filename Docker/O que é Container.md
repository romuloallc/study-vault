Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips

----
- Isolamento
	- File System
	- Processos
	- CPU
	- Memória
	- Disco
	- Usuário
- Foi possível devido:
	- Cgroups 
		- Isolamento de CPU, Memória e disco (I/O)
		- Módulo do Kernel Linux
		- Limitar uso de recursos
	- Namespaces
		- Módulos do Kernel Linux
		- Isolar usuários, filesystem, processos, network
	- Chroot
		- Limitar a visão do usuário
- Compartilha o mesmo Kernel do S.O host
- Imagem do container:
	- Enxuta
	- Tem apenas o que a aplicação precisa
	- Utiliza o Kernel do próprio host
	- Recursos compartilhados, mas isolados
	- Portabilidade
