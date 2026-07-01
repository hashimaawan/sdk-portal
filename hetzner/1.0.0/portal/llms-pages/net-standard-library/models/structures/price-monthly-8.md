# Price Monthly 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTg

Monthly costs for a Load Balancer type in this network zone


# Class Name

`PriceMonthly8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Gross` | `string` | Required | Price with VAT added |
| `Net` | `string` | Required | Price without VAT |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

PriceMonthly8 priceMonthly8 = new PriceMonthly8
{
    Gross = "1.1900000000000000",
    Net = "1.0000000000",
};
```



