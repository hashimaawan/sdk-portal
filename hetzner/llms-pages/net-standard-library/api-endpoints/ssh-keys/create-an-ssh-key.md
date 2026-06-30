# Create an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkNyZWF0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Creates a new SSH key with the given `name` and `public_key`. Once an SSH key is created, it can be used in other calls such as creating Servers.

:information_source: **Note** This endpoint does not require authentication.

```csharp
CreateAnSSHKeyAsync(
    Models.SshKeysRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`SshKeysRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/ssh-keys-request.md) | Body, Optional | - |


# Response Type

**201**: The `ssh_key` key in the reply contains the object that was just created

[`Task<Models.SshKeysResponse1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/ssh-keys-response-1.md)


# Example Usage

```csharp
SshKeysRequest body = new SshKeysRequest
{
    Name = "My ssh key",
    PublicKey = "ssh-rsa AAAjjk76kgf...Xt",
};

try
{
    SshKeysResponse1 result = await sSHKeysController.CreateAnSSHKeyAsync(body);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



