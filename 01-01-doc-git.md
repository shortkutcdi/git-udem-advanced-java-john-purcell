# Git

## git ignore java

https://github.com/github/gitignore/blob/master/Java.gitignore

````.gitignore
# Compiled class file
*.class

# Log file
*.log

# BlueJ files
*.ctxt

# Mobile Tools for Java (J2ME)
.mtj.tmp/

# Package Files #
*.jar
*.war
*.nar
*.ear
*.zip
*.tar.gz
*.rar
````


## git ignore eclipse

````.gitignore
*target*
*.jar
*.war
*.ear
*.class

# eclipse specific git ignore
*.pydevproject
.project
.metadata
bin/**
tmp/**
tmp/**/*
*.tmp
*.bak
*.swp
*~.nib
local.properties
.classpath
.settings/
.loadpath

# External tool builders
.externalToolBuilders/

# Locally stored "Eclipse launch configurations"
*.launch
````

## lancer visual studio à partir terminal

dans un répertoire, lancer visual studio code

    $> code .

## définir vscode comme editeur txt pour git

    $> git config --global core.editor "code"

Définir l'éditeur nano

    $> git config --global core.editor "nano"

## Initialiser un projet git

    $> git init

## Ajouter tous les fichiers

    $> git add *

    $> git add .

## Faire un commit

    $> git commit -m "First commit"

## résumé - git status

    $> git status

## Créer un dépôt github et récupérer dépôt 

    $> git clone <adresse-github du nouveau dépôt>

## git workflow - pousser vers github

Après avoir fait :

- les changements sur les fichiers et dossiers, 
- ajouté les modifications (fichiers/dossiers) - `git add .` 
- vérifié les modifications (optionnel) avec `git status`
- effectué un commit (`git commit -m "changed"`)

On peut pousser le dépôt vers github (distant - remote)

    $> git push origin master 

ici "master" est la branche principale --> elle peut s'appeler "main" dans ce cas remplacer marter par main

    $> git push origin main 

identifiants (credentials) à renseigner une première fois

Donner notre nom et adresse mail pour l'ordinateur

    $ git config --global user.name "Fernand Martinez"
    
    $ git config --global user.email "fernand.martinez22@outlook.fr"

Username for 'https://github.com':  fernand.martinez22@outlook.fr  

ATTENTION - A éviter par soucis de sécurité :
Password for 'https://fernand.martinez22@outlook.fr@github.com':     ****