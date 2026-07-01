# Get an ISO

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRklTT3MlMkZHZXQlMjUyMGFuJTI1MjBJU08

Returns a specific ISO object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAnISOAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the ISO |


# Response Type

**200**: The `iso` key in the reply contains an array of ISO objects with this structure

[`Task<Models.IsosResponse1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/isos-response-1.md)


# Example Usage

```csharp
int id = 112;
try
{
    IsosResponse1 result = await iSOsController.GetAnISOAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



