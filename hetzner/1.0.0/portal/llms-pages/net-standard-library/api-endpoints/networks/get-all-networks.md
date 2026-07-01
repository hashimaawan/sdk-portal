# Get All Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhbGwlMjUyME5ldHdvcmtz

Gets all existing networks that you have available.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllNetworksAsync(
    string name = null,
    string labelSelector = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Query, Optional | Can be used to filter networks by their name. The response will only contain the networks matching the specified name. |
| `labelSelector` | `string` | Query, Optional | Can be used to filter networks by labels. The response will only contain networks with a matching label selector pattern. |


# Response Type

**200**: The `networks` key contains a list of networks

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.NetworksResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/networks-response.md).


# Example Usage

```csharp
try
{
    ApiResponse<NetworksResponse> result = await networksApi.GetAllNetworksAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



