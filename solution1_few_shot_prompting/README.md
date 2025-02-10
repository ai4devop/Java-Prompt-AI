# 📝 Exercise1 - Few-Shot Prompting ~ 10 minutes
Few-shot prompting involves providing the model with a few examples of inputs and outputs to indicate the type of task to perform. It's a simple and intuitive method that can be used for various tasks like code generation or feature verification.

## 1️⃣ Use Case 1: Create a Prompt for the Model to Generate a Java method
Possible example:
```java
// Create a method that checks if a number is even or odd.
// The method isEvenOrOdd called with the parameter 3, like this isEvenOrOdd(3), should return "odd"
// The method isEvenOrOdd called with the parameter 4, like this isEvenOrOdd(4), should return "even"
```

Now it's your turn to integrate your prompt below: 👀
```java
Generate a method in java that accept a number and return odd if it is odd or even of it is even
```

What was the response?
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

## 2️⃣ Use Case 2: Create a New Prompt for the Model to Generate a Java method with a Specific Response Structure
Possible example:
```java
// Can you create a Java method that checks if a word is a palindrome by describing in your own words what a palindrome is without saying the word palindrome?
// Input: isPalindrome("radar") > Output: true
// Input: isPalindrome("Bonjour") > Output: false
```

Now it's your turn to integrate your prompt below: 👀
```java
Generate a java method that take a string in parameter and verify if it can be read in both ways like radar or kayak
```

What was the response?
```java
public class Main {
    public static boolean isPalindrome(String word) {
        String reversed = new StringBuilder(word).reverse().toString();
        return word.equals(reversed);
    }
}
```

## 3️⃣ Use Case 3: Compare Your Two Responses and Test Other Response Structures
Feel free to experiment with different prompts to see how the model adapts and generates varied structures or solutions.
