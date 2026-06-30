# Get All Load Balancers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwYWxsJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnM

Gets all existing Load Balancers that you have available.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<LoadBalancersResponse> getAllLoadBalancersAsync(
    final SortEnum sort,
    final String name,
    final String labelSelector)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`SortEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `load_balancers` key contains a list of Load Balancers

[`LoadBalancersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/load-balancers-response.md)


# Example Usage

```java
loadBalancersController.getAllLoadBalancersAsync(null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



