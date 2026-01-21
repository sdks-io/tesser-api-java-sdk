# Health

```java
HealthController healthController = client.getHealthController();
```

## Class Name

`HealthController`


# Get Health

```java
CompletableFuture<Response> getHealthAsync()
```

## Response Type

[`Response`](../../doc/models/response.md)

## Example Usage

```java
healthController.getHealthAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

