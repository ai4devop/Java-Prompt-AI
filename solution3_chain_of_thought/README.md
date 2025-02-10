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
Voici mon code :
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

Écris une documentation pour ce service API.
```

Quelle a été la réponse ?

```java
## API de gestion des clients

### Introduction
Ce service API permet de gérer les informations des clients via deux endpoints : un pour obtenir les informations d'un client spécifique et un pour mettre à jour les informations d'un client.

### Endpoints

#### 1. GET /clients/{clientId}
- **Description** : Récupère les informations d'un client en fonction de son identifiant.
- **Paramètre** : `clientId` (string) – l’identifiant du client.
- **Exemple de réponse** : John Doe

#### 2. POST /clients
- **Description** : Met à jour les informations d'un client.
- **Exemple de réponse** : Client updated!

### Utilisation
Pour utiliser ce service API, envoyez des requêtes HTTP aux endpoints spécifiés en utilisant l’URL de base.
**Exemple d’utilisation avec curl :**

```bash
# Récupérer les informations d’un client
curl http://localhost:8080/clients/123

# Mettre à jour un client
curl -X POST http://localhost:8080/clients -d "Client updated!"
```

## ## Cas d'usage 2 : Créez un prompt qui demande au modèle de générer la documentation pour la même API, mais cette fois-ci en utilisant une méthodologie spécifique.

Exemple possible :

```java
Créez un prompt qui demande au modèle de générer la documentation pour la même API, mais cette fois-ci en utilisant une méthodologie spécifique comme OpenAPI
```

À vous de jouer en intégrant votre prompt ci-dessous :

```java
Écris une documentation pour ce service API en utilisant la méthodologie OpenAPI.
```
Quelle a été la réponse ?

```java
openapi: 3.0.0
info:
  title: API de gestion des clients
  description: API pour récupérer et mettre à jour des informations de clients.
  version: 1.0.0

paths:
  /clients/{clientId}:
    get:
      summary: Récupérer les informations d'un client
      parameters:
        - in: path
          name: clientId
          required: true
          schema:
            type: string
          description: L'identifiant du client à récupérer.
      responses:
        '200':
          description: Succès
          content:
            application/json:
              schema:
                type: string
              example: John Doe

  /clients:
    post:
      summary: Mettre à jour un client
      requestBody:
        required: true
        content:
          application/json:
            schema:
              type: string
      responses:
        '200':
          description: Succès
          content:
            application/json:
              schema:
                type: string
              example: Client updated!
```
## Cas d'usage 3 : Comparez vos deux réponses et testez d’autres méthodologies ou plans personnalisés
