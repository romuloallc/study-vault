Subject: [[AWS]] 
Type: [[Formação DevOps Professional]]  #aws  #linuxtips 

---
- Imagens que podem ser utilizadas para criar EC2
	- Quickstart AMIs
	- AMIs customs
	- AWS Marketplace AMIs
	- Community AMIs
- Root device type: ebs
- Virtualization: hvm
- Quanto maior a capacidade computacional maior o custo
- Recursos que variam nas instâncias:
	- CPU
	- Memória
	- Disco (Storage)
	- Rede
	- Aceleração
		- GPU
- Família t
	- Aceleração: 
		- Se utilizada abaixo do limite, ela acumula créditos
		- E quando necessário ela pode passar o limite de 100% utilizando esses créditos acumulados
- Cada aplicação vai ter seu tipo de disco ideal
- EBS-optimized instance
	- Outra saída de rede para o disco
	- Separando e melhorando performance
	- ideal para aplicações que usam extensivamente dados em disco (Banco de dados)
- User data <--> Startup script