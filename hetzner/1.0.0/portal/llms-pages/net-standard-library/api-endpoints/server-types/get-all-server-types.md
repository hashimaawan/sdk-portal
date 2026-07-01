# Get All Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwVHlwZXMlMkZHZXQlMjUyMGFsbCUyNTIwU2VydmVyJTI1MjBUeXBlcw

Gets all Server type objects.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllServerTypesAsync(
    string name = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Query, Optional | Can be used to filter Server types by their name. The response will only contain the Server type matching the specified name. |


# Response Type

**200**: The `server_types` key in the reply contains an array of Server type objects with this structure

[`Task<Models.ServerTypesResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-types-response.md)


# Example Usage

```csharp
try
{
    ServerTypesResponse result = await serverTypesController.GetAllServerTypesAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



