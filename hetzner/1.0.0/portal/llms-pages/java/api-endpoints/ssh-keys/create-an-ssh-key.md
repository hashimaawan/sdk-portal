# Create an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkNyZWF0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Creates a new SSH key with the given `name` and `public_key`. Once an SSH key is created, it can be used in other calls such as creating Servers.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<SshKeysResponse1>> createAnSshKeyAsync(
    final SshKeysRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`SshKeysRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ssh-keys-request.md) | Body, Optional | - |


# Response Type

**201**: The `ssh_key` key in the reply contains the object that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`SshKeysResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ssh-keys-response-1.md).


# Example Usage

```java
SshKeysRequest body = new SshKeysRequest.Builder(
    "My ssh key",
    "ssh-rsa AAAjjk76kgf...Xt"
)
.build();

sshKeysApi.createAnSshKeyAsync(body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



