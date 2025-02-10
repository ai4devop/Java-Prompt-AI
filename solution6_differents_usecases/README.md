# 📝 Exercise6 - Different usecases ~ 20 minutes
This file contains several exercises that highlight various use cases for a developer. These exercises will allow you to test multiple scenarios, providing a comprehensive understanding of different situations you may encounter in development.

## Use Case 1: Fix code
Possible example:
```java
// Check why this code is not working whithout IA
// Ask AI to fix it
public static int divide(int a, String b) {
    // Division
    int result = a / b;
    int result = 0;
    return result;
}
```

Now it's your turn to integrate your prompt below: 👀
```java
Why is my code not working ?
public static int divide(int a, String b) {
    // Division
    int result = a / b;
    int result = 0;
    return result;
}
```

What was the response?
```java
Your code has a few issues:

You are trying to divide an integer by a string, which is not allowed.
You have declared the variable result twice, which will cause a compilation error.
Here is the corrected version of your code:

public static int divide(int a, int b) {
    // Division
    int result = 0;
    if (b != 0) {
        result = a / b;
    } else {
        System.out.println("Division by zero is not allowed.");
    }
    return result;
}

This code ensures that the division is performed only if b is not zero, and it handles the case where b is zero by printing an error message.
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
