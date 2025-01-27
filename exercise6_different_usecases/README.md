# 📝 Exercise6 - Different usecases ~ 20 minutes
This file contains several exercises that highlight various use cases for a developer. These exercises will allow you to test multiple scenarios, providing a comprehensive understanding of different situations you may encounter in development.

## Use Case 1: Fix code
Possible example:
```typescript
// Check why this code is not working whithout IA
// Ask AI to fix it
function divide(a: int, b: str) {
    // Division
    let result = a / b;
    result = 0
    return result;
}
```

Now it's your turn to integrate your prompt below: 👀
```typescript
Why is my code not working ?
function divide(a: int, b: str) {
    // Division
    let result = a / b;
    result = 0
    return result;
}
```

What was the response?
```typescript
There are a few issues with your code:

The parameter types are incorrect. The second parameter b should be a number, not a string.
The result is being set to 0 before returning, which means the division result is not being used.
Here is the corrected code:

function divide(a: number, b: number): number {
    // Division
    let result = a / b;
    return result;
}

This code will correctly divide a by b and return the result.
```

## Use Case 2: Optimize code
Possible example:
```typescript
//ask AI to add some optimization like protecting the denominator from 0
function divide(a, b) {
    let result = a / b;
    return result;
}

```

Now it's your turn to integrate your prompt below: 👀
```typescript
Can you add a denominator check to this code ?
function divide(a, b) {
    let result = a / b;
    return result;
}
```

What was the response?
```typescript
function divide(a, b) {
    if (b === 0) {
        throw new Error("Denominator cannot be zero");
    }
    let result = a / b;
    return result;
}
```

## Use Case 3: Reverse engineering
Possible example:
```typescript
// Try to found out what this code do without AI
// Ask AI what is the purpose of this code
// Did you manage to found out before AI ?
function calcul(limit) {
    let primes = [];
    let is_prime = new Array(limit + 1).fill(true);
    let p = 2;

    while (p * p <= limit) {
        if (is_prime[p]) {
            for (let i = p * p; i <= limit; i += p) {
                is_prime[i] = false;
            }
        }
        p += 1;
    }

    for (let p = 2; p <= limit; p++) {
        if (is_prime[p]) {
            primes.push(p);
        }
    }

    return primes;
}

```

Now it's your turn to integrate your prompt below: 👀
```typescript
What does this code do ?
function calcul(limit) {
    let primes = [];
    let is_prime = new Array(limit + 1).fill(true);
    let p = 2;

    while (p * p <= limit) {
        if (is_prime[p]) {
            for (let i = p * p; i <= limit; i += p) {
                is_prime[i] = false;
            }
        }
        p += 1;
    }

    for (let p = 2; p <= limit; p++) {
        if (is_prime[p]) {
            primes.push(p);
        }
    }

    return primes;
}
```

What was the response?
```typescript
The code defines a function calcul that generates a list of prime numbers up to a given limit using the Sieve of Eratosthenes algorithm. Here's a step-by-step explanation:

Initialization:

primes is an empty array that will store the prime numbers.
is_prime is an array of boolean values, initially set to true, indicating that all numbers are considered prime.
p is initialized to 2, the first prime number.
Marking Non-Primes:

The while loop iterates over numbers starting from 2. For each number p, if it is still marked as prime (is_prime[p] is true), it marks all multiples of p as non-prime (false) starting from p * p.
Collecting Primes:

After marking non-prime numbers, the for loop iterates from 2 to the given limit. If a number is still marked as prime (is_prime[p] is true), it is added to the primes array.
Return:

The function returns the primes array containing all prime numbers up to the given limit.
```

## Use Case 4: REGEX
Possible example:
```typescript
// Try to understand what this regex does without AI
// Ask AI what the regex does and compare
// Modify the regex to match your company

^[\w\.=-]+@[\w\.-]+\.[\w]{2,3}$
```

Now it's your turn to integrate your prompt below: 👀
```typescript
Modify this regex ^[\w.=-]+@[\w.-]+.[\w]{2,3}Modify this regex ^[\w.=-]+@[\w.-]+.[\w]{2,3}$ so that it accepts only strings that finish by "@gmail.com"
```

What was the response?
```typescript
^[\w\.=-]+@gmail\.com$
```