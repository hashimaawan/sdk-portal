# Price 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlOA


# Class Name

`Price8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceHourly` | [`PriceHourly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-hourly-7.md) | Required | Hourly costs for a Primary IP type in this Location |
| `PriceMonthly` | [`PriceMonthly9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-monthly-9.md) | Required | Monthly costs for a Primary IP type in this Location |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Price8 price8 = new Price8
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
};
```



