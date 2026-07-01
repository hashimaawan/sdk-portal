# Price per Gb Month

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlUGVyR2JNb250aA


# Class Name

`PricePerGbMonth`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Gross` | `string` | Required | Price with VAT added |
| `Net` | `string` | Required | Price without VAT |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

PricePerGbMonth pricePerGbMonth = new PricePerGbMonth
{
    Gross = "1.1900000000000000",
    Net = "1.0000000000",
};
```



