# Git
Commands and tips about git

[Git](https://git-scm.com/)
 
[GitHub](https://github.com/)
 
# Git commands
 
```
* Configure your name:
git config --global user.name "Jose Lima"
 
* Configure your email:
git config --global user.email "joselima@gmail.com"
 
* Configure Git editor:
git config --global core.editor emacs/vim/vi
 
* View configurations:
git config --list

* Open VSCode to edit configuration in your Git
git config --global -e
 
* Init repository:
git init
 
* Check repository statys:
git status
 
* Add files on Stage:
git add <nome do arquivo> ou git add . (adiciona tudo)
 
* Create a version file:
git commit -m "Descrição da alteração/inclusão"
 
* Check logs:
git log; git log --decorate;
 
* Check logs by author:
git log --author="BRAPAUCO"
 
* Check logs by order alphabetical:
git shortlog; git shortlog -sn
 
* Check logs by graphic:
git log --graph
 
* Search for a specific log:
git show <hash do log em especifico>
 
* View differences:
git diff
 
* View only file name modified:
git diff --name-only
 
* Undo the modifications:
git checkout <nome-do-arquivo>
 
* Remove changes to files on stage:
git reset HEAD <nome-do-arquivo>
 
* Remove change to files committed: git reset --soft --mixed --hard
--soft: Exclui o commit mas deixa o arquivo com as modificações em STAGE
--mixed: Exclui o commit mas deixa o arquivo com as modificações em para adiciona-lás (add)
--hard: Exclui o commit e as alterações do arquivo
 
* Add a remote repository on local machine:
git remote add origin git@github.com:<a-url-do-seu-repositório.git>
 
* Send your modifications to a remote repository:
git push origin -u master
 
* Add and commit your modifications:
git commit -am "New commit"
 
* Clone a repository:
git clone
 
* Create a new branch:
git checkout -b <nome-da-branch>
 
* List all branchs:
git branch
 
* Change the branch:
git checkout <nome-da-branch>
 
* Merge branch:
git merge <nome-da-branch> // Keep history linearly
 
* Rebase branchs:
git rebase <nome-da-branch> // Keep history not linearly
 
* Command to ignore files:
crie o arquivo .gitignore
 
* Keep the changes in a file separated (WIP - Working in progress):
git stash
 
* Apply modifications saved on stash:
git stash apply
 
* Creating alias for commands, example generating alias for status command:
git config --global alias.s status
 
* Version with tags:
git tag -a 1.0.0 -m "Readme finalizado" git push origin master --tags
 
* Erasing what you did wrong without deleting from history what you already did:
git revert <hash do commit que vc quer desfazer>
 
* Erasing tags and branches remotes:
git tag -d <numer-versao-tag>  git push origin :<numero-versao-tag>
```
