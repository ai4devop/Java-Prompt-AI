# 📝 Exercise6 - Different usecases ~ 20 minutes
The fichier contient plusieurs exercices qui mettent en avant plusieurs use cases de développeur. Ces exercices vous permettent de tester plusieurs scénario, permettant de mieux comprendre comment utiliser l'IA dans votre quotidien.

## Cas d'usage 1: Fix code
Exemple possible:
```java
// Vérifiez pourquoi ce code ne fonctionne pas (sans IA)
// Demandez à l'IA de réparer ce code
public static int divide(int a, String b) {
    // Division
    int result = a / b;
    int result = 0;
    return result;
}
```

À vous de jouer en intégrant votre prompt ci-dessous : 👀
```java
Pourquoi mon code ne fonctionne pas
public static int divide(int a, String b) {
    // Division
    int result = a / b;
    int result = 0;
    return result;
}
```

Quelle a été la réponse ?
```java
Votre code ne fonctionne pas pour plusieurs raisons :

Vous essayez de diviser un entier par une chaîne de caractères, ce qui n'est pas possible.
Vous avez deux déclarations de la variable result, ce qui provoque une erreur de compilation.
Voici une version corrigée de votre code :

public static int divide(int a, int b) {
    // Division
    int result = 0;
    if (b != 0) {
        result = a / b;
    } else {
        throw new ArithmeticException("Division by zero is not allowed.");
    }
    return result;
}

Cette version prend deux entiers en entrée et vérifie si le diviseur est différent de zéro avant de procéder à la division. Si le diviseur est zéro, une exception est levée.
```

## Use Case 2: Optimize code
Exemple possible:
```java
// Demandez à l'IA d'ajouter de l'optimisation comme une protection du denominateur différent de 0
public static int divide(int a, int b) {
    int result = a / b;
    return result;
}

```

À vous de jouer en intégrant votre prompt ci-dessous : 👀
```java
Peux-tu ajouter une sécurité pour éviter le dénominateur à 0 ?
public static int divide(int a, int b) {
    int result = a / b;
    return result;
}
```

Quelle a été la réponse ?
```java
public static int divide(int a, int b) {
    if (b == 0) {
        throw new IllegalArgumentException("Le dénominateur ne peut pas être zéro.");
    }
    int result = a / b;
    return result;
}
```

## Use Case 3: Reverse engineering
Exemple possible:
```java
// Demande à l'IA ce que fait ce code
public static List<Integer> calcul(int limit) {
    List<Integer> primes = new ArrayList<>();
    boolean[] isPrime = new boolean[limit + 1];
    
    for (int i = 0; i <= limit; i++) {
        isPrime[i] = true;
    }
    
    int p = 2;
    while (p * p <= limit) {
        if (isPrime[p]) {
            for (int i = p * p; i <= limit; i += p) {
                isPrime[i] = false;
            }
        }
        p++;
    }
    
    for (p = 2; p <= limit; p++) {
        if (isPrime[p]) {
            primes.add(p);
        }
    }
    
    return primes;
}

```

À vous de jouer en intégrant votre prompt ci-dessous : 👀
```java
Que fait ce code ?
public static List<Integer> calcul(int limit) {
    List<Integer> primes = new ArrayList<>();
    boolean[] isPrime = new boolean[limit + 1];
    
    for (int i = 0; i <= limit; i++) {
        isPrime[i] = true;
    }
    
    int p = 2;
    while (p * p <= limit) {
        if (isPrime[p]) {
            for (int i = p * p; i <= limit; i += p) {
                isPrime[i] = false;
            }
        }
        p++;
    }
    
    for (p = 2; p <= limit; p++) {
        if (isPrime[p]) {
            primes.add(p);
        }
    }
    
    return primes;
}
```

Quelle a été la réponse ?
```java
Ce code implémente l'algorithme du crible d'Ératosthène pour trouver tous les nombres premiers jusqu'à une limite donnée. Voici une explication détaillée :

Initialisation :

Une liste primes est créée pour stocker les nombres premiers.
Un tableau booléen isPrime est initialisé avec true pour toutes les positions de 0 à limit.
Marquage des non-premiers :

On initialise p à 2, le premier nombre premier.
Tant que p * p est inférieur ou égal à limit, on vérifie si isPrime[p] est true.
Si c'est le cas, on marque tous les multiples de p (à partir de p * p) comme non-premiers (false).
On incrémente p et on répète le processus.
Collecte des nombres premiers :

Après avoir marqué tous les non-premiers, on parcourt le tableau isPrime.
Si isPrime[p] est true, p est ajouté à la liste primes.
Retourne la liste des nombres premiers.
```

## Use Case 4: REGEX
Exemple possible:
```java
// Essayez de comprendre cette regex sans utiliser l'IA
// Demandez à l'IA ce que fait ce code et comparer avec votre temps de réflexion
// Modifiez cette regex pour fonctionner pour votre entreprise

^[\w\.=-]+@[\w\.-]+\.[\w]{2,3}$
```

À vous de jouer en intégrant votre prompt ci-dessous : 👀
```java
Modifie cette regex ^[\w.=-]+@[\w.-]+.[\w]{2,3} pour que cela accepts seulement les chaines qui finissent par "@gmail.com"
```

Quelle a été la réponse ?
```java
^[\w\.=-]+@gmail\.com$
```
