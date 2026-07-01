# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type object.*


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Network` | [`Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/network.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

NetworksResponse1 networksResponse1 = new NetworksResponse1
{
    Network = new Network
    {
        Created = "created4",
        Id = 78,
        IpRange = "ip_range6",
        Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        Name = "name4",
        Protection = new Protection11
        {
            Delete = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Routes = new List<Route>
        {
            new Route
            {
                Destination = "destination8",
                Gateway = "gateway6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Route
            {
                Destination = "destination8",
                Gateway = "gateway6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Route
            {
                Destination = "destination8",
                Gateway = "gateway6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Servers = new List<int>
        {
            93,
        },
        Subnets = new List<Subnet>
        {
            new Subnet
            {
                Gateway = "gateway4",
                NetworkZone = "network_zone2",
                Type = Type42.Cloud,
                IpRange = "ip_range6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        LoadBalancers = new List<int>
        {
            208,
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



