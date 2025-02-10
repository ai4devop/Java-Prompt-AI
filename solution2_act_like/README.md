# Exercice 2 - Act Like ~ 10 minutes

L'approche "Act Like" consiste à demander au modèle de se comporter comme une personne ou un rôle spécifique. Dans ce cas, nous l’utilisons pour obtenir des conseils sur le développement de fonctionnalités en Java.

## Cas d'usage 1 : Créez un prompt qui demande au modèle de fournir les étapes de développement d’un projet Java et de souligner les points d’attention

Exemple possible :

```java
Créez un prompt qui demande au modèle de fournir les étapes de développement d’un projet Java et de souligner les points d’attention.
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Agis comme un développeur Java expérimenté. Que ne faut-il pas oublier pour développer une API sécurisée en Java ?
```

Quelle a été la réponse ?

```java
En tant que développeur Java expérimenté, voici ce qu'il ne faut pas oublier pour développer une API sécurisée :

1. **Validation des entrées** : Utilisez des bibliothèques comme `Hibernate Validator` pour valider les données entrantes et empêcher les injections SQL ou autres attaques basées sur les entrées utilisateur.

2. **Gestion des erreurs** : Implémentez une gestion cohérente des erreurs pour que l’API renvoie des messages appropriés sans exposer d’informations sensibles.

3. **Authentification et autorisation** : Configurez l'authentification avec JWT et vérifiez que les utilisateurs ont les droits nécessaires pour accéder aux routes.

4. **Chiffrement des données sensibles** : Utilisez des bibliothèques comme `Java Cryptography Extension (JCE)` pour chiffrer les données sensibles, notamment les mots de passe, avant de les stocker.

5. **Tests de sécurité** : Rédigez des tests unitaires et d’intégration avec des outils comme `JUnit` pour assurer la sécurité et le bon fonctionnement de l'API.
```

## Cas d'usage 2 : Créez un prompt qui demande au modèle de vous aider en jouant le rôle d’un expert spécialisé.

Exemple possible :

```java
Créez un prompt qui demande au modèle de vous aider en jouant le rôle d’un expert spécialisé.

```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Agis comme un expert en sécurité des applications web. Que faut-il absolument intégrer dans une API Java pour qu'elle soit conforme aux standards OWASP ?
```
Quelle a été la réponse ?

```java
En tant qu'expert en sécurité des applications web, voici ce qu'il faut intégrer dans une API Java pour être conforme aux standards OWASP :

1. **Prévention des injections** : Utilisez des ORM comme Hibernate pour interagir avec votre base de données et éviter les injections SQL.

2. **Sécurisation de la gestion des sessions** : Assurez-vous que les tokens JWT sont signés et ont une durée de vie limitée pour prévenir toute exploitation.

3. **Chiffrement des données sensibles** : Les données sensibles comme les mots de passe ou les informations personnelles doivent être chiffrées avant d'être stockées.

4. **Gestion des erreurs sans fuite d'informations** : Ne retournez jamais les erreurs complètes aux utilisateurs finaux. Utilisez un middleware de gestion d’erreurs pour renvoyer des messages génériques.

5. **Protection contre les attaques CSRF et XSS** : Utilisez des tokens CSRF et validez les entrées utilisateur pour éviter les attaques XSS.
```
## Cas d'usage 3 : Comparez vos deux réponses et testez d'autres structures de réponses

Exemple possible :

```java
Comparez vos deux réponses et testez d’autres structures de réponses
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Agis comme un Lead Dev Java dans une équipe de développement. Quels sont les principes de conception à ne jamais oublier lors de la création d’un nouveau service en Java ?
```

Quelle a été la réponse ?

```java
En tant que Lead Dev Java, voici les principes de conception à ne jamais oublier :

1. **Principes SOLID** : Assurez-vous que chaque module et méthode respecte les principes SOLID pour un code maintenable et évolutif.

2. **Types stricts et typage avancé** : Utilisez les fonctionnalités de typage avancées de Java, comme les génériques et les interfaces, pour renforcer la robustesse du code.

3. **Testabilité** : Concentrez-vous sur l’écriture de code modulaire et testable. Chaque service devrait être accompagné de tests unitaires et d’intégration.

4. **Modèles de conception** : Utilisez des modèles de conception adaptés tels que le pattern "Repository" pour gérer les interactions avec la base de données.

5. **Documentation claire** : Documentez chaque méthode et classe pour faciliter le travail des autres développeurs et assurer la cohérence dans l’équipe.
```
