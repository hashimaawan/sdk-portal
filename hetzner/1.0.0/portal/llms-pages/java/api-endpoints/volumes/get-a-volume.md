# Get a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZHZXQlMjUyMGElMjUyMFZvbHVtZQ

Gets a specific Volume object.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<VolumesResponse2>> getAVolumeAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Volume |


# Response Type

**200**: The `volume` key contains the volume

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`VolumesResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/volumes-response-2.md).


# Example Usage

```java
int id = 112;

volumesApi.getAVolumeAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



