# Floating Ip 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA0

The cost of one Floating IP per month


# Class Name

`FloatingIp4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PriceMonthly` | [`PriceMonthly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/price-monthly-6.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

FloatingIp4 floatingIp4 = new FloatingIp4
{
    PriceMonthly = new PriceMonthly6
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
    },
};
```



