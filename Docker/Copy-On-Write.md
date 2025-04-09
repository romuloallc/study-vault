Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips 

----
- Imutabilidade da imagem original
- Alterações na cópia
- Imagem de container é **read-only**
- Última camada será possível modificar quando container em execução **nunca a imagem**
- Docker utiliza um esquema de camadas/layers
- Container é uma pilha de camadas compostas de N camadas read-only e uma, a superior, read-write