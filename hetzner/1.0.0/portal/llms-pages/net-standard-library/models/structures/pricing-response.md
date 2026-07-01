# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl


# Class Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pricing` | [`Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/pricing.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

PricingResponse pricingResponse = new PricingResponse
{
    Pricing = new Pricing
    {
        Currency = "EUR",
        FloatingIp = new FloatingIp4
        {
            PriceMonthly = new PriceMonthly6
            {
                Gross = "1.1900000000000000",
                Net = "1.0000000000",
            },
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
                        },
                    },
                },
                Type = Type48Enum.Ipv4,
            },
        },
        Image = new Image3
        {
            PricePerGbMonth = new PricePerGbMonth
            {
                Gross = "1.1900000000000000",
                Net = "1.0000000000",
            },
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
                        },
                        PriceMonthly = new PriceMonthly8
                        {
                            Gross = "1.1900000000000000",
                            Net = "1.0000000000",
                        },
                    },
                },
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
                        },
                        PriceMonthly = new PriceMonthly9
                        {
                            Gross = "1.1900000000000000",
                            Net = "1.0000000000",
                        },
                    },
                },
                Type = Type49Enum.Ipv4,
            },
        },
        ServerBackup = new ServerBackup
        {
            Percentage = "20.0000000000",
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
                        },
                        PriceMonthly = new PriceMonthly10
                        {
                            Gross = "1.1900000000000000",
                            Net = "1.0000000000",
                        },
                    },
                },
            },
        },
        Traffic = new Traffic
        {
            PricePerTb = new PricePerTb
            {
                Gross = "1.1900000000000000",
                Net = "1.0000000000",
            },
        },
        VatRate = "19.000000",
        Volume = new Volume
        {
            PricePerGbMonth = new PricePerGbMonth
            {
                Gross = "1.1900000000000000",
                Net = "1.0000000000",
            },
        },
    },
};
```



