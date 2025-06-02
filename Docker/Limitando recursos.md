Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips 

----
- Limitar a utilização dos recursos do host por parte do container
	- CPU
		- ```docker container run --cpus <n_cpus>```
		- NanoCpus
		- Aceita valores decimais - 0.1
	- Memória
		- ```docker container run --memory <n_memory>```
		- Possível limitar a memória SWAP também
			- ```--memory-swap <n_memory>
- Consumo de recursos:
	- ```docker top```
	- ```docker stats```
