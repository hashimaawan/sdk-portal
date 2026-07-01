# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Network` | [`Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/network.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using HetznerCloudAPI.Standard.Utilities;
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
        },
        Routes = new List<Route>
        {
            new Route
            {
                Destination = "destination8",
                Gateway = "gateway6",
            },
            new Route
            {
                Destination = "destination8",
                Gateway = "gateway6",
            },
            new Route
            {
                Destination = "destination8",
                Gateway = "gateway6",
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
                Type = Type42Enum.Cloud,
                IpRange = "ip_range6",
            },
        },
        LoadBalancers = new List<int>
        {
            208,
        },
    },
};
```



