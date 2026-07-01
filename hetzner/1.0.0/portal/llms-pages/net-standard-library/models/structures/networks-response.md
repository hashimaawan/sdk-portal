# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ


# Class Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `Networks` | [`List<Network>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/network.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using HetznerCloudAPI.Standard.Utilities;
using System.Collections.Generic;

NetworksResponse networksResponse = new NetworksResponse
{
    Networks = new List<Network>
    {
        new Network
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
        },
    },
    Meta = new Meta
    {
        Pagination = new Pagination
        {
            LastPage = 77.7,
            NextPage = 209.18,
            Page = 17.58,
            PerPage = 13.34,
            PreviousPage = 50.02,
            TotalEntries = 206.64,
        },
    },
};
```



