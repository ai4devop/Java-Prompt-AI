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

Now it's yoNow it's your turn to integrate your prompt below: 👀
```java
Write your prompt here
```

What was the response?
```java
Write AI response here
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
Write your prompt here
```

What was the response?
```java
Write AI response here
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
Write your prompt here
```

What was the response?
```java
Write AI response here
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
Write your prompt here
```

What was the response?
```java
Write AI response here
```