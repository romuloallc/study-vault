Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips 

----
- Repositório público e privado de imagens
- Compartilhamento de imagens de pessoas ou empresas
- É possível utilizar um registry local ou em outra nuvem
- Docker Hub é o mais popular
	- Utilizar imagens oficiais
	- Sempre observar de quem é a imagem

```[bash]
docker inspect -f [campo-docker-inspect]
```

- Entender as camadas da imagem:
```[bash]
docker history [imagem]
```
- ImageLayers - docker history online, não precisa baixar a imagem


- Docker Distribution
	- Registry local