# Get a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Returns a specific Primary IP object.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<PrimaryIPResponse> getAPrimaryIPAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**200**: The `primary_ip` key contains a Primary IP object

[`PrimaryIPResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/primary-ip-response.md)


# Example Usage

```java
int id = 112;

primaryIPsController.getAPrimaryIPAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



