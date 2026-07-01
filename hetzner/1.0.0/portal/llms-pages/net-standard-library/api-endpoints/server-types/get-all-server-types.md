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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ServerTypesResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-types-response.md).


# Example Usage

```csharp
try
{
    ApiResponse<ServerTypesResponse> result = await serverTypesApi.GetAllServerTypesAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



