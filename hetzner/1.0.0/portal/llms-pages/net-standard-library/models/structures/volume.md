# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-per-gb-month.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Volume volume = new Volume
{
    PricePerGbMonth = new PricePerGbMonth
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
    },
};
```



