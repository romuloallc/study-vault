---
id: Docker Networking
aliases: []
tags: []
---

Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips 

----
-  Overlay 
	-  Mesma rede no cluster entre todos os nós
	-  Docker Swarm (Deprecated)
-  Bridge
	-  Modo default do Docker
	-  Rede simples e isolada no mesmo host
-  Host
	-  Utilizando a mesma rede do Host
	-  Não recomendado
-  MAC VLAN
	-  Endereço MAC para os containers
	-  Utilizado quando é necessário que os containers se pareçam com hosts físicos na rede
-  None
	-  Sem "interface" de rede
-  IP VLAN
	-  Similar ao MAC VLAN - mas não dá um endereço MAC para o container
	-  Utilizado quando há restrição de endereço MAC na rede
-  Network Plugins
	-  Plugins desenvolvido por terceiros

-  Containers na mesma rede conseguem se comunicar através do nome do container
