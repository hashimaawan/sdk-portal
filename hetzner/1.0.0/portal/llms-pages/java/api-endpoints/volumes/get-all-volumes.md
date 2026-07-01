# Get All Volumes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZHZXQlMjUyMGFsbCUyNTIwVm9sdW1lcw

Gets all existing Volumes that you have available.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<VolumesResponse>> getAllVolumesAsync(
    final Status23 status,
    final Sort sort,
    final String name,
    final String labelSelector)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Volumes matching the status. |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `volumes` key contains a list of volumes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`VolumesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/volumes-response.md).


# Example Usage

```java
volumesApi.getAllVolumesAsync(null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



