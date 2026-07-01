# Get All Primary I Ps

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYWxsJTI1MjBQcmltYXJ5JTI1MjBJUHM

Returns all Primary IP objects.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<PrimaryIPsResponse>> getAllPrimaryIPsAsync(
    final String name,
    final String labelSelector,
    final String ip,
    final Sort2 sort)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `ip` | `String` | Query, Optional | Can be used to filter resources by their ip. The response will only contain the resources matching the specified ip. |
| `sort` | [`Sort2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/sort-2.md) | Query, Optional | Can be used multiple times. Choices id id:asc id:desc created created:asc created:desc |


# Response Type

**200**: The `primary_ips` key contains an array of Primary IP objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PrimaryIPsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/primary-i-ps-response.md).


# Example Usage

```java
String ip = "127.0.0.1";

primaryIPsApi.getAllPrimaryIPsAsync(null, null, ip, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



