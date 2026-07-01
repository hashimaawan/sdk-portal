# Delete an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkRlbGV0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Deletes an SSH key. It cannot be used anymore.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Void>> deleteAnSshKeyAsync(
    final String id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | ID of the SSH key |


# Response Type

**204**: SSH key deleted

`void`


# Example Usage

```java
String id = "id0";

sshKeysApi.deleteAnSshKeyAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



