<h1 align="center">Comandos-Git</h1>

<h2>Principais comandos do git</h2>

-Configurações
```
git config --local user.name "Seu nome aqui"
git config --local user.email "seu@email.aqui"
```

-Para inicializar o git em um diretório (dentro do diretório)
```
git init
```

-Para ver o status do repositório (ver as alterações)
```
git status
```

-Para deixar os arquivos modificados na staging area
```
git add <file> or git add .
```

-Para commitar
```
git commit -m "mensagem do commit"
```

-Para listagem de commits
```
git log, git log --oneline, git log -p
```
estes são os principais mas pode ser útil olhar o ```git log --help```

OBS: Arquivo .gitignore - para mostrar tudo que o git deve ignorar exemplo
```
arquivo.ex
pasta/
```

-Para vincular o repositório com algum servidor
```
git remote add <nome para o servidor> <caminho>
```

-Para alterar o nome do servidor
```
git remote rename <nome antigo> <novo nome>
```

-Para clonar um repositório
```
git clone <caminho>
```

-Para visualizar os repositórios remotos que temos vínculo
```
git remote
```
parâmetro ```-v``` para mostrar o caminho

-Para enviarmos nossos commits para o servidor
```
git push <nome servidor> <branch a ser enviada>
```
caso coloque entre o ```push``` e o ```<nome do servidor>``` o parâmetro ```-u``` nos próximos não será mais necessário colocar o ```<nome servidor> <branch a ser enviada>```

-Para trazer do servidor
```
git pull <nome do servidor> <branch>
```

-Para ver os branches
```
git branch
```

-Para criar uma nova branch
```
git branch <nome branch>
```

-Para alternar para outra branch
```
git checkout <branch que deseja ir>
```

-Para criar uma branch e automáticamente já trocar para ela
```
git checkout -b <nome da branch>
```

-Para fazer um merge
(junta os trabalhos e cria um merge commit)
```
git merge <nome da branch que deseja trazer as alterações>
```

-Para fazer um rebase
(aplica os commits de outra branch na atual)
```
git rebase <branch que deseja trazer os commits>
```
