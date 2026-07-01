# Get a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZHZXQlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Returns a specific Floating IP object.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<FloatingIpsResponse2>> getAFloatingIpAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |


# Response Type

**200**: The `floating_ip` key in the reply contains a Floating IP object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`FloatingIpsResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/floating-ips-response-2.md).


# Example Usage

```java
int id = 112;

floatingIPsApi.getAFloatingIpAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



