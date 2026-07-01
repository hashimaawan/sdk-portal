# Servers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type object.*


# Class Name

`ServersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `Servers` | [`List<Server18>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-18.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

ServersResponse serversResponse = new ServersResponse
{
    Servers = new List<Server18>
    {
        new Server18
        {
            BackupWindow = "22-02",
            Created = "2016-01-30T23:55:00+00:00",
            Datacenter = new Datacenter6
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
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Id = 42,
            Image = new Image
            {
                BoundTo = null,
                Created = "2016-01-30T23:55:00+00:00",
                CreatedFrom = new CreatedFrom
                {
                    Id = 1,
                    Name = "Server",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Deleted = null,
                Deprecated = "2018-02-28T00:00:00+00:00",
                Description = "Ubuntu 20.04 Standard 64 bit",
                DiskSize = 10,
                Id = 42,
                ImageSize = 2.3,
                Labels = new Dictionary<string, string>
                {
                    ["key0"] = "labels4",
                },
                Name = "ubuntu-20.04",
                OsFlavor = OsFlavor.Ubuntu,
                OsVersion = "20.04",
                Protection = new Protection
                {
                    Delete = false,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Status = Status24.Unavailable,
                Type = Type22.Snapshot,
                RapidDeploy = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            IncludedTraffic = 654321,
            IngoingTraffic = 123456,
            Iso = new Iso2
            {
                Deprecated = "2018-02-28T00:00:00+00:00",
                Description = "FreeBSD 11.0 x64",
                Id = 42,
                Name = "FreeBSD-11.0-RELEASE-amd64-dvd1",
                Type = Type26.Public,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Labels = new Dictionary<string, string>
            {
                ["key0"] = "labels0",
            },
            Locked = false,
            Name = "my-resource",
            OutgoingTraffic = 123456,
            PrimaryDiskSize = 50,
            PrivateNet = new List<PrivateNet4>
            {
                new PrivateNet4
                {
                    AliasIps = new List<string>
                    {
                        "alias_ips4",
                    },
                    Ip = "10.0.0.2",
                    MacAddress = "86:00:ff:2a:7d:e1",
                    Network = 4711,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Protection = new Protection20
            {
                Delete = false,
                Rebuild = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            PublicNet = new PublicNet4
            {
                FloatingIps = new List<int>
                {
                    478,
                },
                Ipv4 = new Ipv44
                {
                    Blocked = false,
                    DnsPtr = "server01.example.com",
                    Ip = "1.2.3.4",
                    Id = 42,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Ipv6 = new Ipv64
                {
                    Blocked = false,
                    DnsPtr = new List<DnsPtr8>
                    {
                        new DnsPtr8
                        {
                            DnsPtr = "server.example.com",
                            Ip = "2001:db8::1",
                            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        },
                    },
                    Ip = "2001:db8::/64",
                    Id = 42,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Firewalls = new List<ServerPublicNetFirewall>
                {
                    new ServerPublicNetFirewall
                    {
                        Id = 250,
                        Status = Status72.Applied,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    new ServerPublicNetFirewall
                    {
                        Id = 250,
                        Status = Status72.Applied,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            RescueEnabled = false,
            ServerType = new ServerType1
            {
                Cores = 1,
                CpuType = CpuType.Shared,
                Deprecated = false,
                Description = "CX11",
                Disk = 25,
                Id = 1,
                Memory = 1,
                Name = "cx11",
                Prices = new List<Price9>
                {
                    new Price9
                    {
                        Location = "fsn1",
                        PriceHourly = new PriceHourly8
                        {
                            Gross = "1.1900000000000000",
                            Net = "1.0000000000",
                            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        },
                        PriceMonthly = new PriceMonthly10
                        {
                            Gross = "1.1900000000000000",
                            Net = "1.0000000000",
                            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        },
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                StorageType = StorageType.Local,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Status = Status73.Starting,
            LoadBalancers = new List<int>
            {
                128,
                129,
                130,
            },
            PlacementGroup = new PlacementGroupNullable
            {
                Created = "created8",
                Id = 236,
                Labels = new Dictionary<string, string>
                {
                    ["key0"] = "labels4",
                },
                Name = "name8",
                Servers = new List<int>
                {
                    251,
                    252,
                    253,
                },
                Type = "type2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Volumes = new List<int>
            {
                177,
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



