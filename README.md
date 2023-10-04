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
caso inicialize um como servidor utilizar o parametro ```--bare``` no final

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
Podemos ainda colocar novamente o parâmetro ```-m " descrição" ``` para uma descrição

-Para listagem de commits
```
git log, git log --oneline, git log -p, git log --grep "palavra chave"
```
estes são os principais mas pode ser útil olhar o ```git log --help```

OBS: Arquivo .gitignore - para mostrar tudo que o git deve ignorar, exemplo:
```
arquivo.ex
pasta/
```

-Para vincular o repositório com algum servidor
```
git remote add <nome para o servidor> <caminho>
```
caso seja um caminho de servidor local na máquina recomendavel uso de aspas, ex: "C:/servidor"

-Para alterar o nome do servidor
```
git remote rename <nome antigo> <novo nome>
```

-Para remover um remote
```
git remote rm <nome>
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

-Para excluir um branch
```
git branch -d <nome branch>
```

-Para alternar para outra branch, ou até mesmo para outro commit (por meio do hash)
```
git checkout <branch que deseja ir/ commit que deseja ir>
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

-Para desfazer uma modificação (fora da staging area)
```
git checkout -- <arquivo.ex>
```
(modificações e não commits iniciais - introduzindo o arquivo)

-Para tirar uma modificação da staging area
```
git reset HEAD <arquivo.ex>
```

-Para desfazer um commit (faz um commit novo revertendo)
```
git revert <hash do commit>
```
(o hash pode ser acessado através de um ```git log```)

-Para desfazer um commit (voltando para o estado de um commit sem rastros)
```
git reset --hard [hash do commit que deseja voltar]
```

-Para fazer um stash
```
git stash -m "mensagem"
```

-Para trazer lista de stash e seus respectivos id
```
git stash list
```

-Para trazer de volta do stash
```
git stash apply <id>
```
caso não coloque o id ele trará o primeiro da pilha (útimo a ser colocado id 0)

-Para deletar um stash
```
git stash drop <id>
```
caso não coloque o id ele excluirá o primeiro da pilha (útimo a ser colocado id 0)

-Para trazer de um stash e já apaga-lo
```
git stash pop <id>
```
caso não coloque o id ele fará com o primeiro da pilha (útimo a ser colocado id 0)

-Para limpar todos os stashs
```
git stash clear
```

-Para ver as diferenças das modificações fora da staging area
```
git diff
```

-Para ver as diferenças entre dois commits
```
git diff <hash do commit inicial>..<hash do commit final>
```

Para ver as alterações feitas em um commit
```
git show hash-do-commit
```

-Para criar uma tag
```
git tag -a <nome tag> -m "mensagem"
```

-Para ver as tags disponíveis
```
git tag
```

-Para enviarmos nossas tags para o servidor
```
git push <nome servidor> <nome tag>
```

-Para ver um histórico completo de logs, inclusive de commits deletados
```
git reflog
```
