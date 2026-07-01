# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB


# Class Name

`Traffic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PricePerTb` | [`PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-per-tb.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Traffic traffic = new Traffic
{
    PricePerTb = new PricePerTb
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
    },
};
```



