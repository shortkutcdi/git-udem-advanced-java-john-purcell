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

    $> git status
    $> git add *
    $> git commit -m "Changed to Hello world 2"
    $> git status

Pousser vers le remote - github

    $> git push origin main  -- ou master selon le nom de la branche

