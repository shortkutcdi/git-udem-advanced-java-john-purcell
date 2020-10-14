# Eclipse and git

Créer un projet

Clic/droit/show in local terminal/ Git bash

## Initialiser git

Dans le terminal bash

    $> git init
    
## Ajouter un .gitignore

    $> git code .gitignore

````.gitignore
/bin/
  
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

# virtual machine crash logs, see http://www.java.com/en/download/help/error_hotspot.xml
hs_err_pid*

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

    $> git status

affiche

    ## No commits yet on master
    ?? .gitignore
    ?? src/
    
    $> git add .gitignore
    $> git add *
    $> git commit -m ""