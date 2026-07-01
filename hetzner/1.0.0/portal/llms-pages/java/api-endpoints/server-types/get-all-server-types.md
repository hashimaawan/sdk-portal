# Get All Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwVHlwZXMlMkZHZXQlMjUyMGFsbCUyNTIwU2VydmVyJTI1MjBUeXBlcw

Gets all Server type objects.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ServerTypesResponse> getAllServerTypesAsync(
    final String name)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | Can be used to filter Server types by their name. The response will only contain the Server type matching the specified name. |


# Response Type

**200**: The `server_types` key in the reply contains an array of Server type objects with this structure

[`ServerTypesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-types-response.md)


# Example Usage

```java
serverTypesController.getAllServerTypesAsync(null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



