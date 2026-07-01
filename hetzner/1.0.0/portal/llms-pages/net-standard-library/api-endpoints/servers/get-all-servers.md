# Get All Servers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyMGFsbCUyNTIwU2VydmVycw

Returns all existing Server objects

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllServersAsync(
    string name = null,
    string labelSelector = null,
    Models.Sort? sort = null,
    Models.Status70? status = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `sort` | [`Sort?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`Status70?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/status-70.md) | Query, Optional | Can be used multiple times. The response will only contain Server matching the status |


# Response Type

**200**: A paged array of servers

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ServersResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/servers-response.md).


# Example Usage

```csharp
try
{
    ApiResponse<ServersResponse> result = await serversApi.GetAllServersAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



