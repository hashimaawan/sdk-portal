# Get a Datacenter

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkRhdGFjZW50ZXJzJTJGR2V0JTI1MjBhJTI1MjBEYXRhY2VudGVy

Returns a specific Datacenter object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetADatacenterAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Datacenter |


# Response Type

**200**: The `datacenter` key in the reply contains a Datacenter object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.DatacentersResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/datacenters-response-1.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<DatacentersResponse1> result = await datacentersApi.GetADatacenterAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



