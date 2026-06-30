# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Prices` | [`List<Price6>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/price-6.md) | Required | Floating IP type costs per Location |
| `Type` | [`Type48Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-48.md) | Required | The type of the Floating IP |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

FloatingIp5 floatingIp5 = new FloatingIp5
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
};
```



