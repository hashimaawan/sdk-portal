# Image 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlMw

The cost of Image per GB/month


# Class Name

`Image3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/price-per-gb-month.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Image3 image3 = new Image3
{
    PricePerGbMonth = new PricePerGbMonth
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
    },
};
```



