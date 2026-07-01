# Delete an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkltYWdlcyUyRkRlbGV0ZSUyNTIwYW4lMjUyMEltYWdl

Deletes an Image. Only Images of type `snapshot` and `backup` can be deleted.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> deleteAnImageAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Image |


# Response Type

**204**: Image deleted

`void`


# Example Usage

```java
int id = 112;

imagesApi.deleteAnImageAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



