# Get All Load Balancers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwYWxsJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnM

Gets all existing Load Balancers that you have available.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<LoadBalancersResponse>> getAllLoadBalancersAsync(
    final Sort sort,
    final String name,
    final String labelSelector)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `load_balancers` key contains a list of Load Balancers

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`LoadBalancersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancers-response.md).


# Example Usage

```java
loadBalancersApi.getAllLoadBalancersAsync(null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



