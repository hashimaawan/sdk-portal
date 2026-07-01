# Floating Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FloatingIps` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/floating-ip.md) | Required | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

FloatingIpsResponse floatingIpsResponse = new FloatingIpsResponse
{
    FloatingIps = new List<FloatingIp>
    {
        new FloatingIp
        {
            Blocked = false,
            Created = "2016-01-30T23:55:00+00:00",
            Description = "this describes my resource",
            DnsPtr = new List<DnsPtr>
            {
                new DnsPtr
                {
                    DnsPtrProp = "server.example.com",
                    Ip = "2001:db8::1",
                },
            },
            HomeLocation = new HomeLocation
            {
                City = "Falkenstein",
                Country = "DE",
                Description = "Falkenstein DC Park 1",
                Id = 1,
                Latitude = 50.47612,
                Longitude = 12.370071,
                Name = "fsn1",
                NetworkZone = "eu-central",
            },
            Id = 42,
            Ip = "131.232.99.1",
            Labels = new Dictionary<string, string>
            {
                ["key0"] = "labels2",
            },
            Name = "my-resource",
            Protection = new Protection
            {
                Delete = false,
            },
            Server = 42,
            Type = Type16Enum.Ipv4,
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



