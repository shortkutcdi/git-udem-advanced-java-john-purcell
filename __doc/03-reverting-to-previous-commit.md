# Reverting to previous commit

Modifions App.java - ajoutons "1"

````java
public class App {
    public static void main(String[] args) {
        System.out.println("Hello world 1");
    }
}
````

Ajouter les changements 

    $> git add *
    $> git commit -m "Changed to Hello world 1"

Nouvelle modification App.java modifions "1" en "2"

````java
public class App {
    public static void main(String[] args) {
        System.out.println("Hello world 2");
    }
}
````

Ajouter les changements 

    $> git add *
    $> git commit -m "Changed to Hello world 2"
    $> git status

Pousser vers le remote - github

    $> git push origin main  -- ou master selon le nom de la branche

## Afficher les différents commits - log

Rappel alias git log -- git lg -- permet d'avoir une version plus succinte de git log - avec un graphe des branches

Ajouter un alias - lg et s

    >$ git config --global alias.lg "log --oneline --decorate --all --graph"
    >$ git config --global alias.s "status -s -b"

Afficher les commit - git log

    $> git log
ou 

    $> git lg
    
affiche

    * 4eadebb (HEAD -> main, origin/main, origin/HEAD) Changed to Hello world 2
    * d92904a Changed to Hello world 1
    * f402333 Update file git-branch
    * 81183e8 New Update File doc
    * 69e501e Update documentation
    * 2269fd5 Update message
    * ac20c76 First commit
    * f5bd920 Initial commit
    
## Revenir sur un commit via son hashcode - git checkout <hashcode_du_commit>

    $> git checkout d92904a

    $> git lg

    * 4eadebb (origin/main, origin/HEAD, main) Changed to Hello world 2
    * d92904a (HEAD) Changed to Hello world 1
    * f402333 Update file git-branch

    $> git branch

affiche --> on n'est plus sur main

    * (HEAD detached at d92904a)
      main

revenir à main

    $> git checkout master
    
## Définir une nouvelle branche sur le hashcode d'un commit

    git checkout -b <nom-nouvelle-branche> <hashcode_du_commit>

on veut définir une nouvelle branche `testbranch` sur le commit :  `d92904a Changed to Hello world 1`

    $> git checkout -b testbranch d92904a
    $> git lg
    
affiche - le commit "hello world 1" est passé dans une nouvelle branche `testbranch`

    * 4eadebb (origin/main, origin/HEAD, main) Changed to Hello world 2
    * d92904a (HEAD -> testbranch) Changed to Hello world 1
    * f402333 Update file git-branch
    * 81183e8 New Update File doc

Revenir à la branche main

    $> git checkout main
    
Aller sur la nouvelle branche `testbranch`

    $> git checkout testbranch

Supprimons la nouvelle branche `testbranch` qui n'est plus utile

    $> git checkout main -- revenir sur la branche principale avant de supprimer ou merger
    $> git branch -d testbranch
    $> git lg
    
affiche

    * 4eadebb (HEAD -> main, origin/main, origin/HEAD) Changed to Hello world 2
    * d92904a Changed to Hello world 1
    * f402333 Update file git-branch
    * 81183e8 New Update File doc

