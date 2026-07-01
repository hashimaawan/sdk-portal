# Price 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlOQ


# Class Name

`Price9`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceHourly` | [`PriceHourly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-hourly-8.md) | Required | Hourly costs for a Server type in this Location |
| `PriceMonthly` | [`PriceMonthly10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-monthly-10.md) | Required | Monthly costs for a Server type in this Location |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Price9 price9 = new Price9
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
};
```



