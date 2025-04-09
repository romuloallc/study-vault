Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips 

----
- Grupos que controlam certos recursos. Exemplos:
	- cpu
	- memory
	- blkio
	- devices
	- freezer
- cgtools
	- cgget
	- cgcreate
	- cgset
	- cgclassify
- /sys/fs/cgroup
- Limitar uso de recursos
	- Quotas de CPU
		- /sys/fs/cgroup/cpu
	- Quotas de Memória
		- /sys/fs/cgroup/memory