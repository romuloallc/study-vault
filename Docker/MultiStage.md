Subject: [[Docker]] 
Type: [[Formação DevOps Professional]]  #docker #linuxtips 

----
- Manter imagens pequenas
- Otimize as imagens
	- Alpine Linux - distro bem enxuta
- Pode ser encarado como uma pipeline no **dockerfile**
- Bastante utilizado com linguagens compiladas, como C ou Go

```[bash]
FROM [image-base] AS [stage]
```