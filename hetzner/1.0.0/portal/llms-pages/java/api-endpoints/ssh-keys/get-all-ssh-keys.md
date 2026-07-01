# Get All SSH Keys

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkdldCUyNTIwYWxsJTI1MjBTU0glMjUyMGtleXM

Returns all SSH key objects.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<SshKeysResponse>> getAllSshKeysAsync(
    final Sort8 sort,
    final String name,
    final String fingerprint,
    final String labelSelector)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/sort-8.md) | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `fingerprint` | `String` | Query, Optional | Can be used to filter SSH keys by their fingerprint. The response will only contain the SSH key matching the specified fingerprint. |
| `labelSelector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `ssh_keys` key in the reply contains an array of SSH key objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`SshKeysResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ssh-keys-response.md).


# Example Usage

```java
sshKeysApi.getAllSshKeysAsync(null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



