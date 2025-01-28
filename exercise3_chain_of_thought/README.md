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
Write your prompt here
```

What was the response?
```java
Write AI response here
```

## 2️⃣ Use Case 2: Create a Prompt for the Model to Document the Same API Using a Specific Methodology

Possible example:

```java
Write documentation for this API service using the OpenAPI methodology.
```

Now it's your turn to integrate your prompt below: 👀
```java
Write your prompt here
```

What was the response?
```java
Write AI response here
```

## 3️⃣ Use Case 3: Compare Your Two Responses and Test Other Methodologies or Custom Plans

Feel free to explore other documentation methodologies or customize plans to test how the model adapts to different structures and requirements.
