# Delete a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZEZWxldGUlMjUyMGElMjUyMFZvbHVtZQ

Deletes a volume. All Volume data is irreversibly destroyed. The Volume must not be attached to a Server and it must not have delete protection enabled.

:information_source: **Note** This endpoint does not require authentication.

```csharp
DeleteAVolumeAsync(
    string id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | ID of the Volume |


# Response Type

**204**: Volume deleted

`Task`


# Example Usage

```csharp
string id = "id0";
try
{
    await volumesController.DeleteAVolumeAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



