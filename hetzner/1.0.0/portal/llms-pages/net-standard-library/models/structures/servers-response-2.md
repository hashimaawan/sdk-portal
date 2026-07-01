# Servers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMg


# Class Name

`ServersResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-18.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ServersResponse2 serversResponse2 = new ServersResponse2
{
    Server = new Server18
    {
        BackupWindow = "backup_window2",
        Created = "created4",
        Datacenter = new Datacenter6
        {
            Description = "description0",
            Id = 200,
            Location = new Location
            {
                City = "city6",
                Country = "country8",
                Description = "description6",
                Id = 187.14,
                Latitude = 194.62,
                Longitude = 59.18,
                Name = "name4",
                NetworkZone = "network_zone2",
            },
            Name = "name0",
            ServerTypes = new ServerTypes
            {
                Available = new List<double>
                {
                    23.74,
                },
                AvailableForMigration = new List<double>
                {
                    201.65,
                    201.66,
                },
                Supported = new List<double>
                {
                    69.52,
                    69.53,
                    69.54,
                },
            },
        },
        Id = 14,
        Image = new Image
        {
            BoundTo = 186,
            Created = "created6",
            CreatedFrom = new CreatedFrom
            {
                Id = 60,
                Name = "name6",
            },
            Deleted = "deleted4",
            Deprecated = "deprecated8",
            Description = "description6",
            DiskSize = 244.18,
            Id = 128,
            ImageSize = 141.34,
            Labels = new Dictionary<string, string>
            {
                ["key0"] = "labels4",
            },
            Name = "name6",
            OsFlavor = OsFlavorEnum.Debian,
            OsVersion = "os_version4",
            Protection = new Protection
            {
                Delete = false,
            },
            Status = Status24Enum.Unavailable,
            Type = Type22Enum.App,
            RapidDeploy = false,
        },
        IncludedTraffic = 123.68,
        IngoingTraffic = 151.82,
        Iso = new Iso2
        {
            Deprecated = "deprecated0",
            Description = "description2",
            Id = 66,
            Name = "name8",
            Type = Type26Enum.Public,
        },
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels0",
            ["key1"] = "labels9",
        },
        Locked = false,
        Name = "name4",
        OutgoingTraffic = 129.6,
        PrimaryDiskSize = 19.88,
        PrivateNet = new List<PrivateNet4>
        {
            new PrivateNet4
            {
                AliasIps = new List<string>
                {
                    "alias_ips4",
                },
                Ip = "ip6",
                MacAddress = "mac_address0",
                Network = 154,
            },
            new PrivateNet4
            {
                AliasIps = new List<string>
                {
                    "alias_ips4",
                },
                Ip = "ip6",
                MacAddress = "mac_address0",
                Network = 154,
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
                54,
                55,
                56,
            },
            Ipv4 = new Ipv44
            {
                Blocked = false,
                DnsPtr = "dns_ptr4",
                Ip = "ip2",
                Id = 104,
            },
            Ipv6 = new Ipv64
            {
                Blocked = false,
                DnsPtr = new List<DnsPtr8>
                {
                    new DnsPtr8
                    {
                        DnsPtr = "dns_ptr0",
                        Ip = "ip6",
                    },
                    new DnsPtr8
                    {
                        DnsPtr = "dns_ptr0",
                        Ip = "ip6",
                    },
                },
                Ip = "ip0",
                Id = 8,
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
            Cores = 12.84,
            CpuType = CpuTypeEnum.Shared,
            Deprecated = false,
            Description = "description0",
            Disk = 14.32,
            Id = 30,
            Memory = 21.2,
            Name = "name0",
            Prices = new List<Price9>
            {
                new Price9
                {
                    Location = "location8",
                    PriceHourly = new PriceHourly8
                    {
                        Gross = "gross4",
                        Net = "net2",
                    },
                    PriceMonthly = new PriceMonthly10
                    {
                        Gross = "gross2",
                        Net = "net0",
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



