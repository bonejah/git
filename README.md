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


k: 2
p: [1, 4, 4, 3, 1, 2, 6]
q: [1, 2, 3, 4, 5, 6, 7]
   [2, 3, 3, 3, 0, 0, 0]

Nesse caso, 
k = 2, 
p = [1, 4, 4, 3, 1, 2, 6] e 
q = [1, 2, 3, 4, 5, 6, 7]. 

Em q [0], o ônibus chega no horário 1, então a pessoa número 2 será a última pessoa a pegar o ônibus. Em q [1], o ônibus chega no horário 2, então a pessoa número 3 será a última pessoa a pegar o ônibus como k = 2 e a pessoa número 1 já terá expirado sua paciência até então. Em q [2], o ônibus chega no horário 3, então a pessoa número 3 será a última pessoa a pegar o ônibus como k = 2 e a pessoa número 1 já terá expirado sua paciência até então. Em q [3], o ônibus chega no horário 4, então a pessoa número 3 será a última a pegar o ônibus como k = 2 e a pessoa número 1 já terá expirado sua paciência até então. No q [4], o ônibus chega no horário 5, todos, exceto a última pessoa, teriam expirado sua paciência. Portanto, apenas 1 pessoa entra no ônibus, ele não atende à capacidade e a resposta é 0. E assim por diante para q [5] e q [6].

q[0] = 1
q[1] = 2
q[2] = 3
q[3] = 4
q[4] = 5
q[5] = 6
q[6] = 7

============================================================================================


Por exemplo, dado um 
tamanho de barramento k = 2, 
limites de paciência de p = [1, 2, 3, 4] e 
consultas às vezes q = [1, 3, 4], 

há três cenários, todos lidando com a mesma inicial fila. Onde o ônibus chega a q [0] = 1, todos os passageiros ainda estão na fila, mas apenas os dois primeiros cabem no ônibus. O último passageiro que vai caber é o número 2. Se o ônibus chegar a q [1] = 3, os passageiros 1 e 2 deixaram a fila, os dois primeiros restantes (3 e 4) entram no ônibus, enchendo-o de capacidade. Quando q [2] = 4, os passageiros 1, 2 e 3 foram embora, para que o passageiro 4 possa entrar. Como o ônibus não está cheio, não há um k-ésimo passageiro. A matriz de respostas retornada é [2, 4, 0].   

q[0] = 1 -> entram p1 e p2
q[1] = 3 -> entram p3 e p4
q[2] = 4 -> ???
resp: [2, 4, 0]


==========================================
capacity_bus =                3
number_people_in_the_queue =  3
patience =                    [2, 5, 3]
num_queries =                 [2, 1, 5]

q[0] = 1 => 3 people [1, 2, 3]
q[1] = 5 => 1 people [ , 2,  ]
