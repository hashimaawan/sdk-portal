# Primary I Ps Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlByaW1hcnlJUHNSZXNwb25zZQ


# Class Name

`PrimaryIPsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `PrimaryIps` | [`List<PrimaryIP1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/primary-ip-1.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

PrimaryIPsResponse primaryIPsResponse = new PrimaryIPsResponse
{
    PrimaryIps = new List<PrimaryIP1>
    {
        new PrimaryIP1
        {
            AssigneeId = 17,
            AssigneeType = "server",
            AutoDelete = true,
            Blocked = false,
            Created = "2016-01-30T23:55:00+00:00",
            Datacenter = new Datacenter2
            {
                Description = "Falkenstein DC Park 8",
                Id = 42,
                Location = new Location
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
                Name = "fsn1-dc8",
                ServerTypes = new ServerTypes
                {
                    Available = new List<double>
                    {
                        1,
                        2,
                        3,
                    },
                    AvailableForMigration = new List<double>
                    {
                        1,
                        2,
                        3,
                    },
                    Supported = new List<double>
                    {
                        1,
                        2,
                        3,
                    },
                },
            },
            DnsPtr = new List<DnsPtr>
            {
                new DnsPtr
                {
                    DnsPtrProp = "server.example.com",
                    Ip = "2001:db8::1",
                },
            },
            Id = 42,
            Ip = "131.232.99.1",
            Labels = new Dictionary<string, string>
            {
                ["key0"] = "labels2",
                ["key1"] = "labels3",
                ["key2"] = "labels4",
            },
            Name = "my-resource",
            Protection = new Protection
            {
                Delete = false,
            },
            Type = Type50Enum.Ipv4,
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



