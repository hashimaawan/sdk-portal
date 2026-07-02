# V2 Droplets Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DropletsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Droplet` | [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/droplet.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2DropletsResponse1 v2DropletsResponse1 = new V2DropletsResponse1
{
    Droplet = new Droplet
    {
        BackupIds = new List<int>
        {
            156,
            157,
            158,
        },
        CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        Disk = 150,
        Features = new List<string>
        {
            "features1",
        },
        Id = 28,
        Image = new Image1
        {
            CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Description = "description6",
            Distribution = Distribution.CoreOs,
            ErrorMessage = "error_message8",
            Id = 128,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Locked = false,
        Memory = 64,
        Name = "name0",
        Networks = new Networks
        {
            V4 = new List<V4>
            {
                new V4
                {
                    Gateway = "gateway2",
                    IpAddress = "ip_address2",
                    Netmask = "netmask2",
                    Type = Type10.Public,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new V4
                {
                    Gateway = "gateway2",
                    IpAddress = "ip_address2",
                    Netmask = "netmask2",
                    Type = Type10.Public,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new V4
                {
                    Gateway = "gateway2",
                    IpAddress = "ip_address2",
                    Netmask = "netmask2",
                    Type = Type10.Public,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            V6 = new List<V6>
            {
                new V6
                {
                    Gateway = "gateway4",
                    IpAddress = "ip_address4",
                    Netmask = 106,
                    Type = Type11.Public,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new V6
                {
                    Gateway = "gateway4",
                    IpAddress = "ip_address4",
                    Netmask = 106,
                    Type = Type11.Public,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        NextBackupWindow = new NextBackupWindow
        {
            End = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Start = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Region = new Region
        {
            Available = false,
            Features = new List<string>
            {
                "features7",
                "features8",
                "features9",
            },
            Name = "name6",
            Sizes = new List<string>
            {
                "sizes6",
            },
            Slug = "slug0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Size = new Size
        {
            Available = false,
            Description = "description0",
            Disk = 252,
            Memory = 168,
            PriceHourly = 121.04,
            PriceMonthly = 162.04,
            Regions = new List<string>
            {
                "regions5",
            },
            Slug = "slug6",
            Transfer = 150.78,
            Vcpus = 234,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        SizeSlug = "size_slug0",
        SnapshotIds = new List<int>
        {
            145,
            146,
            147,
        },
        Status = Status8.New,
        Tags = new List<string>
        {
            "tags5",
            "tags6",
        },
        Vcpus = 132,
        VolumeIds = new List<string>
        {
            "volume_ids0",
        },
        Kernel = new Kernel
        {
            Id = 16,
            Name = "name4",
            Version = "version0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        VpcUuid = "vpc_uuid0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



