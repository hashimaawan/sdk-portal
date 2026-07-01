# Delete an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkltYWdlcyUyRkRlbGV0ZSUyNTIwYW4lMjUyMEltYWdl

Deletes an Image. Only Images of type `snapshot` and `backup` can be deleted.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> deleteAnImageAsync(
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

imagesController.deleteAnImageAsync(id).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



