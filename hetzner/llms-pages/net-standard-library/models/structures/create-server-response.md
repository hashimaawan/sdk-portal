# Create Server Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlc3BvbnNl


# Class Name

`CreateServerResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action.md) | Required | - |
| `NextActions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action.md) | Required | - |
| `RootPassword` | `string` | Required | Root password when no SSH keys have been specified |
| `Server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/server-18.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

CreateServerResponse createServerResponse = new CreateServerResponse
{
    Action = new Action
    {
        Command = "start_server",
        Error = new Error
        {
            Code = "action_failed",
            Message = "Action failed",
        },
        Finished = "2016-01-30T23:55:00+00:00",
        Id = 42,
        Progress = 100,
        Resources = new List<Resource>
        {
            new Resource
            {
                Id = 42,
                Type = "server",
            },
        },
        Started = "2016-01-30T23:55:00+00:00",
        Status = StatusEnum.Running,
    },
    NextActions = new List<Action>
    {
        new Action
        {
            Command = "start_server",
            Error = new Error
            {
                Code = "action_failed",
                Message = "Action failed",
            },
            Finished = "2016-01-30T23:55:00+00:00",
            Id = 42,
            Progress = 100,
            Resources = new List<Resource>
            {
                new Resource
                {
                    Id = 42,
                    Type = "server",
                },
            },
            Started = "2016-01-30T23:55:00+00:00",
            Status = StatusEnum.Success,
        },
    },
    RootPassword = "YItygq1v3GYjjMomLaKc",
    Server = new Server18
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
        Id = 42,
        Image = new Image
        {
            BoundTo = null,
            Created = "2016-01-30T23:55:00+00:00",
            CreatedFrom = new CreatedFrom
            {
                Id = 1,
                Name = "Server",
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
            OsFlavor = OsFlavorEnum.Ubuntu,
            OsVersion = "20.04",
            Protection = new Protection
            {
                Delete = false,
            },
            Status = Status24Enum.Unavailable,
            Type = Type22Enum.Snapshot,
            RapidDeploy = false,
        },
        IncludedTraffic = 654321,
        IngoingTraffic = 123456,
        Iso = new Iso2
        {
            Deprecated = "2018-02-28T00:00:00+00:00",
            Description = "FreeBSD 11.0 x64",
            Id = 42,
            Name = "FreeBSD-11.0-RELEASE-amd64-dvd1",
            Type = Type26Enum.Public,
        },
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels0",
            ["key1"] = "labels9",
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
            },
        },
        Protection = new Protection20
        {
            Delete = false,
            Rebuild = false,
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
                    },
                },
                Ip = "2001:db8::/64",
                Id = 42,
            },
            Firewalls = new List<ServerPublicNetFirewall>
            {
                new ServerPublicNetFirewall
                {
                    Id = 250,
                    Status = Status72Enum.Applied,
                },
                new ServerPublicNetFirewall
                {
                    Id = 250,
                    Status = Status72Enum.Applied,
                },
            },
        },
        RescueEnabled = false,
        ServerType = new ServerType1
        {
            Cores = 1,
            CpuType = CpuTypeEnum.Shared,
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
                    },
                    PriceMonthly = new PriceMonthly10
                    {
                        Gross = "1.1900000000000000",
                        Net = "1.0000000000",
                    },
                },
            },
            StorageType = StorageTypeEnum.Local,
        },
        Status = Status73Enum.Starting,
        LoadBalancers = new List<int>
        {
            144,
            143,
            142,
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
        },
        Volumes = new List<int>
        {
            91,
            92,
        },
    },
};
```



