# Delete an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkRlbGV0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Deletes an SSH key. It cannot be used anymore.

:information_source: **Note** This endpoint does not require authentication.

```csharp
DeleteAnSSHKeyAsync(
    string id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | ID of the SSH key |


# Response Type

**204**: SSH key deleted

`Task`


# Example Usage

```csharp
string id = "id0";
try
{
    await sSHKeysController.DeleteAnSSHKeyAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



