Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips 

----
- Permite o isolamento de processos
- Responsável para que o container tenha seu próprio environment
	- Árvore de processos
	- Pontos de montagem
	- Não interfira na execução de outro
- PID namespace
	- Dentro do container um processo em execução terá um PID
	- Fora do container é possível encontrar esse processo, no entanto, com outro PID
- Net namespace
	- Permite que cada container tenha sua própria interface de rede e portas
	- 2 Net Namespace diferente
		- Um para a interface do container - eth0
		- Um para o host - veth+identificador
	- Interfaces linkadas através da bridge Docker0 no host
- Mnt namespace
	- Cada container tem seu próprio ponto de montagem e seu sistema de arquivos raiz
	- Garante que um processo rodando em um sistema de arquivos não consiga acessar outro sistema de arquivos em outro **Mnt Namespace**
- IPC namespace
	- SystemV IPC isolado
	- Fila de mensagens POSIX própria
- UTS namespace
	- isolamento de hostname, nome de domínio, versão do S.O
- User namespace
	- Responsável pelo mapa de identificação em cada container