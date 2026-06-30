# Price Monthly 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTY


# Class Name

`PriceMonthly6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Gross` | `string` | Required | Price with VAT added |
| `Net` | `string` | Required | Price without VAT |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

PriceMonthly6 priceMonthly6 = new PriceMonthly6
{
    Gross = "1.1900000000000000",
    Net = "1.0000000000",
};
```



