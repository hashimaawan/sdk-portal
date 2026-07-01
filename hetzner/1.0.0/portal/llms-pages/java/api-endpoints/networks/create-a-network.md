# Create a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGQ3JlYXRlJTI1MjBhJTI1MjBOZXR3b3Jr

Creates a network with the specified `ip_range`.

You may specify one or more `subnets`. You can also add more Subnets later by using the [add subnet action](https://docs.hetzner.cloud/#network-actions-add-a-subnet-to-a-network). If you do not specify an `ip_range` in the subnet we will automatically pick the first available /24 range for you.

You may specify one or more routes in `routes`. You can also add more routes later by using the [add route action](https://docs.hetzner.cloud/#network-actions-add-a-route-to-a-network).

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<NetworksResponse1>> createANetworkAsync(
    final CreateNetworkRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/create-network-request.md) | Body, Optional | - |


# Response Type

**201**: The `network` key contains the network that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`NetworksResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/networks-response-1.md).


# Example Usage

```java
CreateNetworkRequest body = new CreateNetworkRequest.Builder(
    "10.0.0.0/16",
    "mynet"
)
.build();

networksApi.createANetworkAsync(body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



