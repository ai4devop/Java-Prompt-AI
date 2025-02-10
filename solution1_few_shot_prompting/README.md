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
Génère une méthode en java qui accepte un nombre et retourne "pair" si c'est pair et "impair" si c'est impair
```

Quelle a été la réponse ?

```java
public class YourClass {
    // ...existing code...

    public String verifierPairImpair(int nombre) {
        if (nombre % 2 == 0) {
            return "pair";
        } else {
            return "impair";
        }
    }

    // ...existing code...
}
```

## Cas d'usage 2 : Créez un nouveau prompt qui demande au modèle de générer une méthode Java avec une structure de réponse spécifique

Exemple possible :

```java
// créez une méthode Java qui vérifie si un mot est un palindrome
// Input: isPalindrome("radar") > Output: true
// Input: isPalindrome("Bonjour") > Output: false
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Génère une méthode en java qui va prendre une chaine de caractères et vérifier s'il peut se lire dans les deux sens comme radar ou kayak
```

```java
public class PalindromeChecker {

    public static boolean isPalindrome(String str) {
        if (str == null) {
            return false;
        }
        int left = 0;
        int right = str.length() - 1;
        
        while (left < right) {
            if (str.charAt(left) != str.charAt(right)) {
                return false;
            }
            left++;
            right--;
        }
        return true;
    }

    public static void main(String[] args) {
        System.out.println(isPalindrome("radar")); // true
        System.out.println(isPalindrome("kayak")); // true
        System.out.println(isPalindrome("hello")); // false
    }
}
```
## Cas d'usage 3 : Comparez vos deux réponses et testez d'autres structures de réponses

Expérimentez différents type de prompt avec et sans exemples afin de comparer les résultats que vous recevez
