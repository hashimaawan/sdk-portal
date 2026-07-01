# Get a SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkdldCUyNTIwYSUyNTIwU1NIJTI1MjBrZXk

Returns a specific SSH key object.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<SshKeysResponse1> getASSHKeyAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the SSH key |


# Response Type

**200**: The `ssh_key` key in the reply contains an SSH key object with this structure

[`SshKeysResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ssh-keys-response-1.md)


# Example Usage

```java
int id = 112;

sSHKeysController.getASSHKeyAsync(id).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



