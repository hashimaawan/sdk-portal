# Price

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNl


# Class Name

`Price`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceHourly` | [`PriceHourly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/price-hourly.md) | Required | Hourly costs for a Resource in this Location |
| `PriceMonthly` | [`PriceMonthly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/price-monthly.md) | Required | Monthly costs for a Resource in this Location |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Price price = new Price
{
    Location = "fsn1",
    PriceHourly = new PriceHourly
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
    },
    PriceMonthly = new PriceMonthly
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
    },
};
```



