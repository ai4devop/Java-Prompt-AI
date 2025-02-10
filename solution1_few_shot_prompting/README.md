# Exercice 1 - Few-Shot Prompting ~ 10 minutes

Le few-shot prompting consiste à fournir au modèle quelques exemples d'entrées et de sorties pour lui indiquer le type de tâche à accomplir. C'est une méthode simple et intuitive, utile pour des tâches variées telles que la génération de code ou la vérification de fonctionnalités.

## Cas d'usage 1 : Créez un prompt qui demande au modèle de générer une méthode Java

Exemple possible :

```bash
// Créez une méthode qui vérifie si un nombre est pair ou impair.
// La méthode isEvenOrOdd appelée avec le paramètre 3, comme ceci isEvenOrOdd(3), doit retourner "Odd".
// La méthode isEvenOrOdd appelée avec le paramètre 4, comme ceci isEvenOrOdd(4), doit retourner "Even".
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Créez un prompt qui demande au modèle de générer une méthode Java.
```

Voici le README.md adapté en Java et en français pour l'exercice de Few-Shot Prompting :

Exercice 1 - Few-Shot Prompting ~ 10 minutes
Le few-shot prompting consiste à fournir au modèle quelques exemples d'entrées et de sorties pour lui indiquer le type de tâche à accomplir. C'est une méthode simple et intuitive, utile pour des tâches variées telles que la génération de code ou la vérification de fonctionnalités.

Cas d'usage 1 : Créez un prompt qui demande au modèle de générer une méthode Java
Exemple possible :

java
Copier le code
// Créez une méthode qui vérifie si un nombre est pair ou impair.
// La méthode isEvenOrOdd appelée avec le paramètre 3, comme ceci isEvenOrOdd(3), doit retourner "Odd".
// La méthode isEvenOrOdd appelée avec le paramètre 4, comme ceci isEvenOrOdd(4), doit retourner "Even".
À vous de jouer en intégrant votre prompt ci-dessous :

Quelle a été la réponse ?

```java
public class Main {
    public static String isEvenOrOdd(int number) {
        if (number % 2 == 0) {
            return "Even";
        }
        return "Odd";
    }
}
```

## Cas d'usage 2 : Créez un nouveau prompt qui demande au modèle de générer une méthode Java avec une structure de réponse spécifique

Exemple possible :

```java
// Peux-tu créer une méthode Java qui vérifie si un mot est un palindrome ?
// Input: isPalindrome("radar") > Output: true
// Input: isPalindrome("Bonjour") > Output: false
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Créez un nouveau prompt qui demande au modèle de générer une méthode Java avec une structure de réponse spécifique.
```

```java
public class Main {
    public static boolean isPalindrome(String word) {
        String reversed = new StringBuilder(word).reverse().toString();
        return word.equals(reversed);
    }
}
```
## Cas d'usage 3 : Comparez vos deux réponses et testez d'autres structures de réponses

Ce fichier README.md explique comment utiliser le few-shot prompting en Java pour générer des méthodes avec des exemples simples. Vous pouvez comparer les réponses et ajuster les prompts pour tester d'autres fonctionnalités de génération de code.
