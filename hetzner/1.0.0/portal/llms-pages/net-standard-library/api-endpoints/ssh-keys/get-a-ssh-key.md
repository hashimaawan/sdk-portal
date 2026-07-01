# Get a SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkdldCUyNTIwYSUyNTIwU1NIJTI1MjBrZXk

Returns a specific SSH key object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetASshKeyAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the SSH key |


# Response Type

**200**: The `ssh_key` key in the reply contains an SSH key object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.SshKeysResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ssh-keys-response-1.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<SshKeysResponse1> result = await sshKeysApi.GetASshKeyAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



