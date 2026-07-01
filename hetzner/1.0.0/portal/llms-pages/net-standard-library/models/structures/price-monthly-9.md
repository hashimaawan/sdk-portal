# Price Monthly 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTk

Monthly costs for a Primary IP type in this Location


# Class Name

`PriceMonthly9`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Gross` | `string` | Required | Price with VAT added |
| `Net` | `string` | Required | Price without VAT |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

PriceMonthly9 priceMonthly9 = new PriceMonthly9
{
    Gross = "1.1900000000000000",
    Net = "1.0000000000",
};
```



