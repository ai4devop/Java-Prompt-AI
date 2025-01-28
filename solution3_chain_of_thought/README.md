# 📝 Exercise3 - Chain of Thought ~ 10 minutes

The "chain of thought" technique involves guiding the model through a reasoning process to explain each step of the thought process. Here, we use this method to generate TypeScript documentation.

## 1️⃣ Use Case 1: Create a Prompt for the Model to Write Documentation for Java Code

Possible example:

```java
Here is my code:
import javax.ws.rs.GET;
import javax.ws.rs.POST;
import javax.ws.rs.Path;
import javax.ws.rs.PathParam;
import javax.ws.rs.core.Response;
import javax.ws.rs.core.Application;
import java.util.HashSet;
import java.util.Set;

@ApplicationPath("/api")
public class ClientApplication extends Application {
    @Override
    public Set<Class<?>> getClasses() {
        Set<Class<?>> resources = new HashSet<>();
        resources.add(ClientResource.class);
        return resources;
    }
}

@Path("/clients")
class ClientResource {

    @GET
    @Path("/{clientId}")
    public Response getClient(@PathParam("clientId") String clientId) {
        return Response.ok("John Doe").build();
    }

    @POST
    public Response updateClient() {
        return Response.ok("Client updated!").build();
    }
}

Write documentation for this API service.
```

Now it's your turn to integrate your prompt below: 👀

```java
Create a prompt for the model to write documentation for Java code.
[code]
```

What was the response?

```markdown
## Client Management API

### Introduction

This API service allows managing client information via two endpoints: one to retrieve information for a specific client and one to update client information.

### Endpoints

#### 1. GET /clients/{clientId}

- **Description**: Retrieves information about a client based on their ID.
- **Parameter**: `clientId` (string) – the client's identifier.
- **Example response**: John Doe

#### 2. POST /clients

- **Description**: Updates a client's information.
- **Example response**: Client updated!

### Usage

To use this API service, send HTTP requests to the specified endpoints using the base URL.
**Example usage with curl:**

# Retrieve client information

curl http://localhost:8080/api/clients/123

# Update a client

curl -X POST http://localhost:8080/api/clients -d "Client updated!"
```

## 2️⃣ Use Case 2: Create a Prompt for the Model to Document the Same API Using a Specific Methodology

Possible example:

```java
Write documentation for this API service using the OpenAPI methodology.
```

Now it's your turn to integrate your prompt below: 👀

```typescript
Create a prompt for the model to document the same API using OpenAPI method.
```

What was the response?

```java
openapi: 3.0.0
info:
  title: Client Management API
  description: API to retrieve and update client information.
  version: 1.0.0
paths:
  /clients/{clientId}:
    get:
      summary: Retrieve client information
      parameters:
        - in: path
          name: clientId
          required: true
          schema:
            type: string
          description: The client's ID to retrieve.
      responses:
        '200':
          description: Success
          content:
            application/json:
              schema:
                type: string
                example: John Doe
  /clients:
    post:
      summary: Update a client
      requestBody:
        required: true
        content:
          application/json:
            schema:
              type: string
      responses:
        '200':
          description: Success
          content:
            application/json:
              schema:
                type: string
                example: Client updated!
```

## 3️⃣ Use Case 3: Compare Your Two Responses and Test Other Methodologies or Custom Plans

Feel free to explore other documentation methodologies or customize plans to test how the model adapts to different structures and requirements.
