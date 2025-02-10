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

Now it's your turn to integrate your prompt below: 👀
```java
Pourquoi mon code ne fonctionne pas
public static int divide(int a, String b) {
    // Division
    int result = a / b;
    int result = 0;
    return result;
}
```

What was the response?
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
Possible example:
```java
//ask AI to add some optimization like protecting the denominator from 0
public static int divide(int a, int b) {
    int result = a / b;
    return result;
}

```

Now it's your turn to integrate your prompt below: 👀
```java
Can you add a denominator check to this code ?
public static int divide(int a, int b) {
    int result = a / b;
    return result;
}
```

What was the response?
```java
public static int divide(int a, int b) {
    if (b == 0) {
        throw new IllegalArgumentException("Denominator cannot be zero");
    }
    int result = a / b;
    return result;
}
```

## Use Case 3: Reverse engineering
Possible example:
```java
// Ask AI what is the purpose of this code
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

Now it's your turn to integrate your prompt below: 👀
```java
What does this code do ?
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

What was the response?
```java
This code implements the Sieve of Eratosthenes algorithm to find all prime numbers up to a given limit. Here's a step-by-step explanation:

Initialization:

A list primes is created to store the prime numbers.
A boolean array isPrime of size limit + 1 is created and initialized to true. This array will be used to mark non-prime numbers.
Marking non-prime numbers:

The algorithm starts with the smallest prime number, p = 2.
For each number p, if isPrime[p] is true, it marks all multiples of p (starting from p * p) as false in the isPrime array.
This process continues until p * p exceeds the limit.
Collecting prime numbers:

After marking non-prime numbers, the algorithm iterates through the isPrime array.
For each index p where isPrime[p] is true, p is added to the primes list.
Returning the result:

The list of prime numbers primes is returned.
```

## Use Case 4: REGEX
Possible example:
```java
// Try to understand what this regex does without AI
// Ask AI what the regex does and compare
// Modify the regex to match your company

^[\w\.=-]+@[\w\.-]+\.[\w]{2,3}$
```

Now it's your turn to integrate your prompt below: 👀
```java
Modify this regex ^[\w.=-]+@[\w.-]+.[\w]{2,3}Modify this regex ^[\w.=-]+@[\w.-]+.[\w]{2,3}$ so that it accepts only strings that finish by "@gmail.com"
```

What was the response?
```java
^[\w\.=-]+@gmail\.com$
```
