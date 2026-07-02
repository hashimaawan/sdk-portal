# Multiple Droplet Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk11bHRpcGxlJTI1MjBEcm9wbGV0JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`MultipleDropletResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Droplets` | [`List<Droplet>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/droplet.md) | Required | - |
| `Links` | [`Links1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/links-1.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

MultipleDropletResponse multipleDropletResponse = new MultipleDropletResponse
{
    Droplets = new List<Droplet>
    {
        new Droplet
        {
            BackupIds = new List<int>
            {
                53893572,
            },
            CreatedAt = DateTime.ParseExact("2020-07-21T18:37:44Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Disk = 25,
            Features = new List<string>
            {
                "backups",
                "private_networking",
                "ipv6",
            },
            Id = 3164444,
            Image = new Image1
            {
                CreatedAt = DateTime.ParseExact("2020-05-04T22:23:02Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                Description = "description6",
                Distribution = Distribution.Ubuntu,
                ErrorMessage = "error_message8",
                Id = 7555620,
                MinDiskSize = 20,
                Name = "Nifty New Snapshot",
                MPublic = true,
                Regions = new List<Region2>
                {
                    Region2.Nyc1,
                    Region2.Nyc2,
                },
                SizeGigabytes = 2.34,
                Slug = "nifty1",
                Status = Status7.New,
                Tags = new List<string>
                {
                    "base-image",
                    "prod",
                },
                Type = Type9.Snapshot,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Locked = false,
            Memory = 1024,
            Name = "example.com",
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
                End = DateTime.ParseExact("2019-12-04T23:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                Start = DateTime.ParseExact("2019-12-04T00:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Region = new Region
            {
                Available = true,
                Features = new List<string>
                {
                    "private_networking",
                    "backups",
                    "ipv6",
                    "metadata",
                    "install_agent",
                    "storage",
                    "image_transfer",
                },
                Name = "New York 3",
                Sizes = new List<string>
                {
                    "s-1vcpu-1gb",
                    "s-1vcpu-2gb",
                    "s-1vcpu-3gb",
                    "s-2vcpu-2gb",
                    "s-3vcpu-1gb",
                    "s-2vcpu-4gb",
                    "s-4vcpu-8gb",
                    "s-6vcpu-16gb",
                    "s-8vcpu-32gb",
                    "s-12vcpu-48gb",
                    "s-16vcpu-64gb",
                    "s-20vcpu-96gb",
                    "s-24vcpu-128gb",
                    "s-32vcpu-192g",
                },
                Slug = "nyc3",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Size = new Size
            {
                Available = true,
                Description = "Basic",
                Disk = 25,
                Memory = 1024,
                PriceHourly = 0.00743999984115362,
                PriceMonthly = 5,
                Regions = new List<string>
                {
                    "ams2",
                    "ams3",
                    "blr1",
                    "fra1",
                    "lon1",
                    "nyc1",
                    "nyc2",
                    "nyc3",
                    "sfo1",
                    "sfo2",
                    "sfo3",
                    "sgp1",
                    "tor1",
                },
                Slug = "s-1vcpu-1gb",
                Transfer = 1,
                Vcpus = 1,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            SizeSlug = "s-1vcpu-1gb",
            SnapshotIds = new List<int>
            {
                67512819,
            },
            Status = Status8.Active,
            Tags = new List<string>
            {
                "web",
                "env:prod",
            },
            Vcpus = 1,
            VolumeIds = new List<string>
            {
                "506f78a4-e098-11e5-ad9f-000f53306ae1",
            },
            Kernel = new Kernel
            {
                Id = 16,
                Name = "name4",
                Version = "version0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            VpcUuid = "760e09ef-dc84-11e8-981e-3cfdfeaae000",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Links = new Links1
    {
        Actions = new List<Action1>
        {
            new Action1
            {
                Href = "href0",
                Id = 154,
                Rel = "rel4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



