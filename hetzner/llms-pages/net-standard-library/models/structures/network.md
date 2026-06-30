# Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRk5ldHdvcms


# Class Name

`Network`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Created` | `string` | Required | Point in time when the Network was created (in ISO-8601 format) |
| `Id` | `int` | Required | ID of the Network |
| `IpRange` | `string` | Required | IPv4 prefix of the whole Network |
| `Labels` | `object` | Required | User-defined labels (key-value pairs) |
| `LoadBalancers` | `List<int>` | Optional | Array of IDs of Load Balancers attached to this Network |
| `Name` | `string` | Required | Name of the Network |
| `Protection` | [`Protection11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/protection-11.md) | Required | Protection configuration for the Network |
| `Routes` | [`List<Route>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/route.md) | Required | Array of routes set in this Network |
| `Servers` | `List<int>` | Required | Array of IDs of Servers attached to this Network |
| `Subnets` | [`List<Subnet>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/subnet.md) | Required | Array subnets allocated in this Network |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using HetznerCloudAPI.Standard.Utilities;
using System.Collections.Generic;

Network network = new Network
{
    Created = "2016-01-30T23:50:00+00:00",
    Id = 4711,
    IpRange = "10.0.0.0/16",
    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    Name = "mynet",
    Protection = new Protection11
    {
        Delete = false,
    },
    Routes = new List<Route>
    {
        new Route
        {
            Destination = "10.100.1.0/24",
            Gateway = "10.0.1.1",
        },
    },
    Servers = new List<int>
    {
        42,
    },
    Subnets = new List<Subnet>
    {
        new Subnet
        {
            Gateway = "10.0.0.1",
            NetworkZone = "eu-central",
            Type = Type42Enum.Cloud,
            IpRange = "10.0.1.0/24",
        },
    },
    LoadBalancers = new List<int>
    {
        42,
    },
};
```



