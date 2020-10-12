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