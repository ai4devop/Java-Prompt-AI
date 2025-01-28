# 📝 Exercise2 - Act Like ~ 10 minutes

"Act like" involves asking the model to behave as a specific person or role. In this case, we use it to get advice on developing features in Java.

## 1️⃣ Use Case 1: Create a Prompt for the Model to Provide Steps for Developing a JAVA Project and Highlight Key Points

Possible example:
```java
Ask your AI like a JAVA developer to help you secure an API in JAVA
```

Now it's your turn to integrate your prompt below: 👀

```java
Act like an experienced JAVA developer. What should not be forgotten when developing a secure API in JAVA?
```

What was the response?
```java
As an experienced Java developer, here’s what should not be forgotten when developing a secure API:
1. **Input Validation**: Use libraries like `Hibernate Validator` or custom validation logic to validate incoming data and prevent SQL injection or other input-based attacks.
2. **Error Handling**: Implement consistent error handling using exceptions and logging so that the API returns appropriate error messages without exposing sensitive information.
3. **Authentication and Authorization**: Implement authentication using methods such as Spring Security and ensure users have appropriate permissions to access routes.
4. **Encryption of Sensitive Data**: Use libraries like `JCA` (Java Cryptography Architecture) to secure sensitive data, especially passwords, before storage.
5. **Security Testing**: Write unit and integration tests with frameworks like `JUnit` and `Mockito` to ensure your API is secure and functions as expected.
```

## 2️⃣ Use Case 2: Create a Prompt for the Model to Assist by Acting as a Specialized Expert

Possible example:
```java
Ask AI to play a role to help you secure your JAVA API to ensure compliance with OWASP standards
```

Now it's your turn to integrate your prompt below: 👀
```java
Act like a web application security expert. What needs to be integrated into a JAVA API to ensure compliance with OWASP standards?
```

What was the response?
```java
As a web application security expert, here’s what should be integrated into a JAVA API for OWASP compliance:
1. **Injection Prevention**: Use ORMs like TypeORM to interact with your database and prevent SQL injection.
2. **Session Management Security**: Ensure JWT tokens are well-signed and have limited lifespan to prevent exploitation.
3. **Encryption of Sensitive Data**: All sensitive data such as passwords or personal information must be encrypted before storage.
4. **Error Management Without Information Leakage**: Never return full errors to end users. Use an error-handling middleware to return generic messages.
5. **Protect Against CSRF and XSS Attacks**: Use CSRF tokens and validate user input to prevent XSS attacks.

By following these recommendations, you’ll ensure compliance with OWASP’s best security practices.
```

## 3️⃣ Use Case 3: Compare Your Two Responses and Test Other Response Structures

Possible example:
```java
Compare your two responses and test other response structures.
```

Now it's your turn to integrate your prompt below: 👀
```java
Act like ....
```

What was the response?
```java
As a Lead Dev Java, here are the design principles to never forget:
1. **SOLID Principles**: Ensure each class and method follows SOLID principles for maintainable and scalable code.
2. **Strict Typing with Java**: Utilize Java's strong type system to enforce robustness and prevent type-related errors.
3. **Testability**: Focus on writing modular and testable code. Utilize frameworks like JUnit for unit and integration tests.
4. **Design Patterns**: Implement design patterns like the "Factory" or "Singleton" pattern where applicable to improve code organization and maintainability.
5. **Clear Documentation**: Use Javadoc to document each function and class to facilitate other developers’ work and ensure team consistency.
```

