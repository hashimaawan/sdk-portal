# Get a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhJTI1MjBOZXR3b3Jr

Gets a specific network object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetANetworkAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the network |


# Response Type

**200**: The `network` key contains the network

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.NetworksResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/networks-response-1.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<NetworksResponse1> result = await networksApi.GetANetworkAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



