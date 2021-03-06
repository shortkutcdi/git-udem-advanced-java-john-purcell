# Git branch

Faire une copie séparée du code provisoire sur une branche
Une fois les modifications réalisées et validées sur la nouvelle branche (sans alterer la branche master), fusionner cette branche sur le master en y incorporant les modification de la branche fusionnée - enfin supprimer la branche devenue inutile

## Créer une branche - testbranch

    $> git branch testbranch 

afficher les branches

    $> git branch

affiche

    * master
    testbranch

## changer de branch - checkout 

passer à la branche `testbranch`

    $> git checkout testbranch

affiche

    Switched to branch 'testbranch'

Vérifier sur quelle branche on se trouve

    $> git branch

affiche (avec *brancheactive)

    master
    * testbranch

## Modification dans la branche testbranch

modifions la classe App ajoutons des !!!

````java
public class App {
    public static void main(String[] args) {
        System.out.println("Hello world!!!");
    }
}
````

vérifions les changements

    $> git status

    On branch testbranch
    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to discard changes in working directory)
            modified:   src/app/App.java

Ajoutons toutes les modifications

    $> git add *
    
    $> git status

    $> git commit -m "Changed message"

Ajout au dépôt distant (remote) - définir la branche

    $> git push origin testbranch

## merge and delete branches

se déplacer dans la branche vers laquelle on va merger (fusionner)

    $> git checkout master

Faire une fusion de la branche `testbranch` (vers la branche actuelle `master`)

    $> git merge testbranch

Supprimer une branche inutile ici `testbranch` avec `git branch -d <branche_a_supprimer>`

    $> git branch -d testbranch

Forcer la suppression avec `-D` (à la place de `-d`)
    
    $> git branch -D testbranch

Vérifier les branches     
    
    $> git branch 

Affiche les branches - la branche testbranche est effacée

    * main

Mettre à jour la suppression sur github (remote)    
    
    $> git push origin --delete testbranch