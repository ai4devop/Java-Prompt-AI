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
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```java
Ecrivez la réponse de l'IA ici
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
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```java
Ecrivez la réponse de l'IA ici
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
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```java
Ecrivez la réponse de l'IA ici
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
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```java
Ecrivez la réponse de l'IA ici
```
