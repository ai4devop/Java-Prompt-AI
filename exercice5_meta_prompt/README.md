# Exercice 5 - Méta-prompt ~ 10 minutes

Le méta-prompt consiste à créer un prompt qui va être une sorte de prompt template à utiliser sur plusieurs occasions.

## Cas d'usage 1 : Créez un prompt qui demande au modèle de créer un prompt pour un sujet.

Exemple possible :

```java
Créez un prompt pour le modèle qui va être une base de prompt et qui peut vous aider dans plusieurs occasions
Par exemple, les best practices pour le développement java 23
(Vous pouvez également demander à l'IA de vous aider pour la créer)
Et utilisez là pour certains use cases
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Ecrivez votre prompt ici
```

```java
Ecrivez la réponse de l'IA ici
```

## Cas d'usage 2 : Créez un prompt qui demande au modèle de créer un prompt combinant plusieurs méthodes de prompting.

Exemple possible :

```java
Écris un prompt IA qui va combiner la méthode "act like" et la méthode "chain of thought" pour générer une liste de bonnes pratiques pour un projet Spring Boot.
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Créez un prompt qui demande au modèle de créer un prompt combinant plusieurs méthodes de prompting.
```
Quelle a été la réponse ?

```java
Voici un prompt combinant la méthode "act like" et la méthode "chain of thought" pour générer des bonnes pratiques pour Spring Boot :

"Agis comme un expert Spring Boot. En utilisant une réflexion par étapes (chain of thought), génère une liste de bonnes pratiques pour développer un projet Spring Boot. Décris chaque bonne pratique en expliquant son importance et comment elle améliore la qualité du projet. Concentre-toi sur l'organisation du code, la sécurité, l'optimisation des performances, les tests et la documentation."
```
## Cas d'usage 3 : Demandez au modèle de s'auto-évaluer et d'améliorer sa réponse.

Exemple possible

```java
La liste de chaînes est-elle suffisante pour tester entièrement la méthode validateEmail ? Sinon, comment peut-elle être améliorée ?
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Demandez au modèle de s'auto-évaluer et d'améliorer sa réponse.
```

Quelle a été la réponse ?

```java
La liste fournie couvre de nombreux cas courants, mais elle peut être améliorée en ajoutant des cas spécifiques aux normes actuelles des e-mails et en prenant en compte certaines configurations plus rares. Voici des points d'amélioration potentiels :

1. **Cas de caractères internationaux** : Ajouter des e-mails avec des caractères Unicode pour tester si la méthode peut gérer des noms d'utilisateur ou des domaines dans d'autres alphabets.
    - Exemple : "名@例.com" (Valide)

2. **Cas de plus de 64 caractères avant le symbole @** : Les adresses e-mail peuvent avoir un maximum de 64 caractères avant le @.
    - Exemple : "longemailaddresslongemailaddresslongemailaddresslongemailaddress@domain.com" (Valide)

3. **Cas de domaine sans extension** : Tester des domaines qui n'ont pas d'extensions de domaine traditionnelles.
    - Exemple : "user@localhost" (Potentiellement valide dans certains environnements)

En prenant en compte ces cas supplémentaires, vous obtiendrez une validation plus complète de la méthode validateEmail.
```

## Analyse des exemples fournis

# Méta-prompt simple : Le premier exercice demande au modèle de générer un prompt pré-écrit efficace dans un bon nombre d'occasion. La solution suggère un prompt bien structuré, couvrant des aspects essentiels comme la sécurité et l’organisation des couches.

# Méta-prompt combiné : Le deuxième exercice utilise les méthodes "act like" et "chain of thought" pour générer un prompt complexe, où le modèle doit réfléchir étape par étape et agir comme un expert. La réponse montre une approche réfléchie pour combiner les deux techniques, offrant des résultats détaillés.
