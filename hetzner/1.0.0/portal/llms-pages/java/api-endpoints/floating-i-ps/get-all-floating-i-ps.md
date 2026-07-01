# Get All Floating I Ps

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZHZXQlMjUyMGFsbCUyNTIwRmxvYXRpbmclMjUyMElQcw

Returns all Floating IP objects.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<FloatingIpsResponse>> getAllFloatingIPsAsync(
    final String name,
    final String labelSelector,
    final Sort2 sort)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | Can be used to filter Floating IPs by their name. The response will only contain the Floating IP matching the specified name. |
| `labelSelector` | `String` | Query, Optional | Can be used to filter Floating IPs by labels. The response will only contain Floating IPs matching the label selector. |
| `sort` | [`Sort2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/sort-2.md) | Query, Optional | Can be used multiple times. Choices id id:asc id:desc created created:asc created:desc |


# Response Type

**200**: The `floating_ips` key in the reply contains an array of Floating IP objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`FloatingIpsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/floating-ips-response.md).


# Example Usage

```java
floatingIPsApi.getAllFloatingIPsAsync(null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



