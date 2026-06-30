# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlByaW1hcnlJcA


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Prices` | [`List<Price8>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/price-8.md) | Required | Primary IP type costs per Location |
| `Type` | [`Type49Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-49.md) | Required | The type of the Primary IP |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

PrimaryIp primaryIp = new PrimaryIp
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
};
```



