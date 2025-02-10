# Exercice 3 - Chain of Thought ~ 10 minutes

La technique "Chain of Thought" consiste à guider le modèle dans un processus de raisonnement pour expliquer chaque étape de réflexion. Ici, nous utilisons cette méthode pour générer de la documentation en Java.

## Cas d'usage 1 : Créez un prompt qui demande au modèle d'écrire de la documentation pour un code Java.

Exemple possible :

```java
Créez un prompt qui demande au modèle d'écrire de la documentation pour un code Java.

import org.springframework.web.bind.annotation.*;

@RestController
@RequestMapping("/clients")
public class ClientController {

    @GetMapping("/{clientId}")
    public String getClient(@PathVariable String clientId) {
        return "John Doe";
    }

    @PostMapping
    public String updateClient() {
        return "Client updated!";
    }
}
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Ecrivez votre prompt ici
```

```java
Ecrivez la réponse de l'IA ici
```

## ## Cas d'usage 2 : Créez un prompt qui demande au modèle de générer la documentation pour la même API, mais cette fois-ci en utilisant une méthodologie spécifique.

Exemple possible :

```java
Créez un prompt qui demande au modèle de générer la documentation pour la même API, mais cette fois-ci en utilisant une méthodologie spécifique comme OpenAPI
```

À vous de jouer en intégrant votre prompt ci-dessous :


```java
Ecrivez votre prompt ici
```

```java
Ecrivez la réponse de l'IA ici
```
## Cas d'usage 3 : Comparez vos deux réponses et testez d’autres méthodologies ou plans personnalisés
