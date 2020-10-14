# git pull

Quand on travail en équipe la version remote (github) peut être màj par un collègue
De ce fait notre version locale n'est plus à jour

`git pull` permet de récupérer la version remote sur notre ordinateur (local)

`history` permet de naviguer dans l'historique des commandes dans le shellbash

## Créons un dossier /tempgit dans lequel on va cloner le repos github 

dans /tempgit :

    $> git clone https://github.com/shortkutcdi/git-udem-advanced-java-john-purcell.git
    
    $> cd /tempgit
    $> ls
    
    git-udem-advanced-java-john-purcell/

    $> cd git-udem-advanced-java-john-purcell/
    $> ls

    
Modifions le fichier readme.md (local) avec nano : `nano README.md`
Modifions le fichier readme.md (local) avec visualstudio code : `code README.md`

````.md
# git-udem-advanced-java-john-purcell

This is the Cave of programming Advanced Java course    

This is an arbitrary pointless change.                 
````
    
Afficher le fichier README.md : `$> cat README.md`    

faisons un ajout+commit avec : `$> git commit -am "Commentaire du commit"`

    $> git commit -am "Made a change to README
    
Enregistrons les changements sur github (remote)

    $> git push origin main
    
##  Résumé

On a 2 Projets git locaux

    + /tempgit
                /git-udem-advanced-java-john-purcell 
    + /git-udem-advanced-java-john-purcell (repo original dont le remote n'est plus à jour)

## Git pull origin -- Récupérer les changements de github vers le repository local 

On va récupérer les changements du remote vers le repot original avec un `pull`

Dans le repot local original Le fichier README.md ne contient qu'un titre

dans le dossier `/git-udem-advanced-java-john-purcell`

    $> git pull origin 

>>> le fichier README.md est mis à jour

## Git push -- enregistrer les changements du repo local vers github (remote)

- (repos local) Modifions le fichier README.md - suppression de la dernière phrase
- Faisons un commit -am (ajout + commit)
- puis ajoutons (poussons) les modifications vers le repo distant github

    $> code README.md 

(modification du fichier README)
    
    $> git commit -am "Remove change to README" // -am  ajout+commit
    $> git push origin main
