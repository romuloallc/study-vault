Type: [[Git]]  #git #youtube  

---
#### Configs iniciais
```[bash]
git config --global user.name <name>
```

```[bash]
git config --global user.email <email>
```

```[bash]
git config --global init.default main
```

- Tipos de config:
	- System
		- Todo o sistema vai ter a mesma configuração do Git
		- Bem pouco utilizado
	- Global
	- Project

#### Comandos
- Iniciar repositório local
```[bash]
git init
```

- Adicionar arquivos na área de staging
```[bash]
git add
```

- Mostrar se tem arquivos em staging ou não
```[bash]
git status
```

- Remove os arquivos da área de staging
```[bash]
git reset
```

- Faz o commit da área de staging
```[bash]
git commit -m <commit-message>
```

- Logs de commits
```[bash]
git log
```

- Vai para o commit selecionado
```[bash]
git checkout <commit-id>
```

- Volta para o top commit da main
```[bash]
git checkout main
```

- Cria uma branch nova
```[bash]
git checkout -b <branch>
```

```[bash]
git switch -c <branch>
```

- Muda de branch
```[bash]
git switch <branch>
```

- Lista branches locais(somente após commit)
```[bash]
git branch
```

- Lista branches remotas
```[bash]
git branch -r
```

- Lista todas as branches
```[bash]
git branch -a
```

- Deleta uma branch
```[bash]
git branch -d <branch>
```

- Faz o merge de uma branch para outra
```[bash]
git merge <branch>
```

#### Repositório remoto

- Adiciona repositório remoto utilizando SSH
```[bash]
git remote add origin git@github.com:<github-user>/<github-repo>
```

- Mapea a branch main local com a branch main remota 
```[bash]
git branch -M main
```

- Faz o push da branch local para branch remota
```[bash]
git push -u origin main
```

- Lista repositórios remotos
```[bash]
git remote -v
```