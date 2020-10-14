# Merge conflicts

Si on a plus d'une personne travaillant sur le même repo

On a 2 Projets git locaux

    + /git-udem-advanced-java-john-purcell            (repo 1)
    + /tempgit
                /git-udem-advanced-java-john-purcell  (repo 2)

Faisons des changement pour créer des conflits    

`Repo 1` - changeons le README.md

````.md
# git-udem-advanced-java-john-purcell

This is the Cave of programming Advanced Java course.

This is an extra line
````

      $> git commit -am "Added line to README"
      $> git push origin main

`Repo 2` - dossier `/tempgit`- changeons le README.md  (différent du précédent)

    $> cd tempgit
    $> cd git-udem-advanced-java-john-purcell
    $> code README.md

````.md
# git-udem-advanced-java-john-purcell

This is the Cave of programming Advanced Java course.

This is some extra line that i'm adding.
````    

  $> git commit -am "Adding an extra line to README"
  $> git push origin main

Affiche une erreur

    To https://github.com/shortkutcdi/git-udem-advanced-java-john-purcell.git
     ! [rejected]        main -> main (fetch first)
    error: failed to push some refs to 'https://github.com/shortkutcdi/git-udem-advanced-java-john-purcell.git'
    hint: Updates were rejected because the remote contains work that you do
    hint: not have locally. This is usually caused by another repository pushing
    hint: to the same ref. You may want to first integrate the remote changes
    hint: (e.g., 'git pull ...') before pushing again.
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.

--> le main remote (github) est différent du main local (dans /tempgit) --> récupérer avec un pull

Récupérer le main remote avec un `git pull    `

    $> git pull origin

Erreur de Merge    

    Auto-merging README.md
    CONFLICT (content): Merge conflict in README.md
    Automatic merge failed; fix conflicts and then commit the result.

    $> code README.md

Affiche

Fichier README.md

````.md
This is the Cave of programming Advanced Java course.

<<<<<<< HEAD (current change)
This is some extra line that i'm adding.
=======
This is an extra line
>>>>>>> 5c86deb546f38551cd1c0c7c50c064f3a6952b02
````

Entre la ligne 76 et 77 ancienne modif --> à garder

Sur vscode on a plusieurs choix
- accept current change
- incomming change (ancien)
- both changes

Fichier README.md

````.md
This is the Cave of programming Advanced Java course.

This is an extra line
````

    $> git status
    affiche >>> both modified:   README.md

    $> git commit -am "Adding an extra line to README"
    $> git push origin main

Sur le `Repo 1` - récupérer le repo remote (github)

    $> git pull origin
    $> code README.md

Affiche

````.md
This is the Cave of programming Advanced Java course.

This is an extra line
````   

## Eviter les conflits

- En équipe ne pas travailler sur le même code
- faire un `git pull origin` avant de commencer des modifications
