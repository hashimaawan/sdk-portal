# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlNw


# Class Name

`Price7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceHourly` | [`PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone |
| `PriceMonthly` | [`PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Price7 price7 = new Price7
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
};
```



