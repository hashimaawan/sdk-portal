# Get All IS Os

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRklTT3MlMkZHZXQlMjUyMGFsbCUyNTIwSVNPcw

Returns all available ISO objects.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllISOsAsync(
    string name = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Query, Optional | Can be used to filter ISOs by their name. The response will only contain the ISO matching the specified name. |


# Response Type

**200**: The `isos` key in the reply contains an array of iso objects with this structure

[`Task<Models.IsosResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/isos-response.md)


# Example Usage

```csharp
try
{
    IsosResponse result = await iSOsController.GetAllISOsAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



