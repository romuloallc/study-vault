Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips 

----
- Arquivo de texto com instruções para construir uma imagem de container
- Instruções em maiúsculo
- Nome do arquivo deve ser: Dockerfile
	- Tem outras formas
- Usar imagens criadas por outras pessoas, através de um Registry, como o Docker Hub
- Use **ENTRYPOINT** e **CMD** no mesmo Dockerfile
- Adicione um non-root user
- Use o .dockerignore
- Use o **RUN** com moderação
- Somente pacotes necessários
- Reduza o número de camadas: Use o Multiline com o RUN
- Limpe a casa
	- Remova pacotes desnecessários 
		- *apt-get clean && rm -rf /var/lib/apt/lists/\**
		- *dnf clean all && rm -rf /var/cache/dnf/\**

FROM -> Imagem base
RUN ->  Executa comando 
EXPOSE -> Porta que irá ser exposta
COPY -> Copia arquivos de algum lugar para dentro do container
WORKDIR -> Muda o diretório de trabalho do **/** para onde o container vai entrar
ENV -> Variáveis de ambiente
ENTRYPOINT -> Comando de entrada para quando o container inicia - Principal processo. 
- Não pode ser sobrescrito
CMD -> Executa o comando após o container iniciar
- Quando o ENTRYPOINT é utilizado junto com o CMD, este atua como parâmetros do comando do ENTRYPOINT
LABEL -> Rótulos para metadatas, gerenciamento, informações
ADD -> Possíbilita pegar coisas da internet
- Arquivos compactados irá jogar o arquivo descompactado, caso esteja local, se tiver na internet vai jogar o arquivo compactado
VOLUME -> Volume a ser montado no container
MAINTAINER -> Autor da imagem
USER -> Usuário que será utilizado na imagem
- Por default é o root
ENV -> Criar a variável de ambiente no container
ARG -> Variável de ambiente no momento de build, mas não existe após o container iniciar
- É possivel passar valores no comando de build - O comando tem precedência
VOLUME -> Cria um volume para que os dados do container persistam em caso de reiniciar ou morrer


##### Build da imagem
- Comando:
```[bash]
docker build -t [repository]/[name]:[version] [path-to-dockerfile]
```
- Exemplo:
```[bash]
docker build -t linuxtips/apache:1.0 .
```

