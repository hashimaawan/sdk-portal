# Get a Datacenter

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkRhdGFjZW50ZXJzJTJGR2V0JTI1MjBhJTI1MjBEYXRhY2VudGVy

Returns a specific Datacenter object.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<DatacentersResponse1>> getADatacenterAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Datacenter |


# Response Type

**200**: The `datacenter` key in the reply contains a Datacenter object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`DatacentersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/datacenters-response-1.md).


# Example Usage

```java
int id = 112;

datacentersApi.getADatacenterAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



