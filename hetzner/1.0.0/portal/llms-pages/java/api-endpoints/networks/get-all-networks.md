# Get All Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhbGwlMjUyME5ldHdvcmtz

Gets all existing networks that you have available.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<NetworksResponse> getAllNetworksAsync(
    final String name,
    final String labelSelector)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | Can be used to filter networks by their name. The response will only contain the networks matching the specified name. |
| `labelSelector` | `String` | Query, Optional | Can be used to filter networks by labels. The response will only contain networks with a matching label selector pattern. |


# Response Type

**200**: The `networks` key contains a list of networks

[`NetworksResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/networks-response.md)


# Example Usage

```java
networksController.getAllNetworksAsync(null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



