# Create a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGQ3JlYXRlJTI1MjBhJTI1MjBOZXR3b3Jr

Creates a network with the specified `ip_range`.

You may specify one or more `subnets`. You can also add more Subnets later by using the [add subnet action](https://docs.hetzner.cloud/#network-actions-add-a-subnet-to-a-network). If you do not specify an `ip_range` in the subnet we will automatically pick the first available /24 range for you.

You may specify one or more routes in `routes`. You can also add more routes later by using the [add route action](https://docs.hetzner.cloud/#network-actions-add-a-route-to-a-network).

:information_source: **Note** This endpoint does not require authentication.

```csharp
CreateANetworkAsync(
    Models.CreateNetworkRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/create-network-request.md) | Body, Optional | - |


# Response Type

**201**: The `network` key contains the network that was just created

[`Task<Models.NetworksResponse1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/networks-response-1.md)


# Example Usage

```csharp
CreateNetworkRequest body = new CreateNetworkRequest
{
    IpRange = "10.0.0.0/16",
    Name = "mynet",
};

try
{
    NetworksResponse1 result = await networksController.CreateANetworkAsync(body);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



