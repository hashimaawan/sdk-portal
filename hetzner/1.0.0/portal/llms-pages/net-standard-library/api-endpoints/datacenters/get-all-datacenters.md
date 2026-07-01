# Get All Datacenters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkRhdGFjZW50ZXJzJTJGR2V0JTI1MjBhbGwlMjUyMERhdGFjZW50ZXJz

Returns all Datacenter objects.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllDatacentersAsync(
    string name = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Query, Optional | Can be used to filter Datacenters by their name. The response will only contain the Datacenter matching the specified name. When the name does not match the Datacenter name format, an `invalid_input` error is returned. |


# Response Type

**200**: The reply contains the `datacenters` and `recommendation` keys

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.DatacentersResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/datacenters-response.md).


# Example Usage

```csharp
try
{
    ApiResponse<DatacentersResponse> result = await datacentersApi.GetAllDatacentersAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



