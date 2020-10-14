# Configurer git (nom & @ mail) de façon globale

Donner notre nom et adresse mail pour l'ordinateur

    $ git config --global user.name "Fernand Martinez"
    
    $ git config --global user.email "fernand.martinez22@outlook.fr"

Ajouter un alias

    >$ git config --global alias.lg "log --oneline --decorate --all --graph"


Vérifier les paramètres saisis

    $ git config --global --list

        user.name=Fernand Martinez
        user.email=fernand.martinez22@outlook.fr
        alias.lg=log --oneline --decorate --all --graph
        alias.s=status -s -b
        color.ui=true

## aide - Afficher les commandes git

    $ git

ou 
    
    $ git --help    