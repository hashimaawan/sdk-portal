# Server Types 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzMg


# Class Name

`ServerTypes2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `double` | Required | ID of the Server type the price is for |
| `Name` | `string` | Required | Name of the Server type the price is for |
| `Prices` | [`List<Price9>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-9.md) | Required | Server type costs per Location |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ServerTypes2 serverTypes2 = new ServerTypes2
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
};
```



