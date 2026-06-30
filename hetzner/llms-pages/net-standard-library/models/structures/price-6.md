# Price 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlNg


# Class Name

`Price6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceMonthly` | [`PriceMonthly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/price-monthly-7.md) | Required | Monthly costs for a Floating IP type in this Location |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Price6 price6 = new Price6
{
    Location = "fsn1",
    PriceMonthly = new PriceMonthly7
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
    },
};
```



