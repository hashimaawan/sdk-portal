# Pricing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNpbmc


# Class Name

`Pricing`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Currency` | `string` | Required | Currency the returned prices are expressed in, coded according to ISO 4217 |
| `FloatingIp` | [`FloatingIp4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/floating-ip-4.md) | Required | The cost of one Floating IP per month |
| `FloatingIps` | [`List<FloatingIp5>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/floating-ip-5.md) | Required | Costs of Floating IPs types per Location and type |
| `Image` | [`Image3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/image-3.md) | Required | The cost of Image per GB/month |
| `LoadBalancerTypes` | [`List<LoadBalancerType6>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-type-6.md) | Required | Costs of Load Balancer types per Location and type |
| `PrimaryIps` | [`List<PrimaryIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/primary-ip.md) | Required | Costs of Primary IPs types per Location |
| `ServerBackup` | [`ServerBackup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-backup.md) | Required | Will increase base Server costs by specific percentage |
| `ServerTypes` | [`List<ServerTypes2>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-types-2.md) | Required | Costs of Server types per Location and type |
| `Traffic` | [`Traffic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/traffic.md) | Required | The cost of additional traffic per TB |
| `VatRate` | `string` | Required | The VAT rate used for calculating prices with VAT |
| `Volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/volume.md) | Required | The cost of Volume per GB/month |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

Pricing pricing = new Pricing
{
    Currency = "EUR",
    FloatingIp = new FloatingIp4
    {
        PriceMonthly = new PriceMonthly6
        {
            Gross = "1.1900000000000000",
            Net = "1.0000000000",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    FloatingIps = new List<FloatingIp5>
    {
        new FloatingIp5
        {
            Prices = new List<Price6>
            {
                new Price6
                {
                    Location = "fsn1",
                    PriceMonthly = new PriceMonthly7
                    {
                        Gross = "1.1900000000000000",
                        Net = "1.0000000000",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Type = Type48.Ipv4,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Image = new Image3
    {
        PricePerGbMonth = new PricePerGbMonth
        {
            Gross = "1.1900000000000000",
            Net = "1.0000000000",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    LoadBalancerTypes = new List<LoadBalancerType6>
    {
        new LoadBalancerType6
        {
            Id = 1,
            Name = "lb11",
            Prices = new List<Price7>
            {
                new Price7
                {
                    Location = "fsn1",
                    PriceHourly = new PriceHourly6
                    {
                        Gross = "1.1900000000000000",
                        Net = "1.0000000000",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    PriceMonthly = new PriceMonthly8
                    {
                        Gross = "1.1900000000000000",
                        Net = "1.0000000000",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    PrimaryIps = new List<PrimaryIp>
    {
        new PrimaryIp
        {
            Prices = new List<Price8>
            {
                new Price8
                {
                    Location = "fsn1",
                    PriceHourly = new PriceHourly7
                    {
                        Gross = "1.1900000000000000",
                        Net = "1.0000000000",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    PriceMonthly = new PriceMonthly9
                    {
                        Gross = "1.1900000000000000",
                        Net = "1.0000000000",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Type = Type49.Ipv4,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ServerBackup = new ServerBackup
    {
        Percentage = "20.0000000000",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ServerTypes = new List<ServerTypes2>
    {
        new ServerTypes2
        {
            Id = 4,
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Traffic = new Traffic
    {
        PricePerTb = new PricePerTb
        {
            Gross = "1.1900000000000000",
            Net = "1.0000000000",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    VatRate = "19.000000",
    Volume = new Volume
    {
        PricePerGbMonth = new PricePerGbMonth
        {
            Gross = "1.1900000000000000",
            Net = "1.0000000000",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
};
```



