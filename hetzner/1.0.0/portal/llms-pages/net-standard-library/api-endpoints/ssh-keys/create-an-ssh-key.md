# Create an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkNyZWF0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Creates a new SSH key with the given `name` and `public_key`. Once an SSH key is created, it can be used in other calls such as creating Servers.

:information_source: **Note** This endpoint does not require authentication.

```csharp
CreateAnSshKeyAsync(
    Models.SshKeysRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`SshKeysRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ssh-keys-request.md) | Body, Optional | - |


# Response Type

**201**: The `ssh_key` key in the reply contains the object that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.SshKeysResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ssh-keys-response-1.md).


# Example Usage

```csharp
SshKeysRequest body = new SshKeysRequest
{
    Name = "My ssh key",
    PublicKey = "ssh-rsa AAAjjk76kgf...Xt",
};

try
{
    ApiResponse<SshKeysResponse1> result = await sshKeysApi.CreateAnSshKeyAsync(body);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



