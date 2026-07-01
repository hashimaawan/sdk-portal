# Get All Servers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyMGFsbCUyNTIwU2VydmVycw

Returns all existing Server objects

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ServersResponse>> getAllServersAsync(
    final String name,
    final String labelSelector,
    final Sort sort,
    final Status70 status)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`Status70`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/status-70.md) | Query, Optional | Can be used multiple times. The response will only contain Server matching the status |


# Response Type

**200**: A paged array of servers

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ServersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/servers-response.md).


# Example Usage

```java
serversApi.getAllServersAsync(null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



