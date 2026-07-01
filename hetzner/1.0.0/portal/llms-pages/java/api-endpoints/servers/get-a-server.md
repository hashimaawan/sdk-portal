# Get a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyMGElMjUyMFNlcnZlcg

Returns a specific Server object. The Server must exist inside the Project

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ServersResponse2>> getAServerAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |


# Response Type

**200**: The `server` key in the reply contains a Server object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ServersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/servers-response-2.md).


# Example Usage

```java
int id = 112;

serversApi.getAServerAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



