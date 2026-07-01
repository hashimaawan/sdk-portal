# Get a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyMGElMjUyMFNlcnZlcg

Returns a specific Server object. The Server must exist inside the Project

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ServersResponse2> getAServerAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |


# Response Type

**200**: The `server` key in the reply contains a Server object with this structure

[`ServersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/servers-response-2.md)


# Example Usage

```java
int id = 112;

serversController.getAServerAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



