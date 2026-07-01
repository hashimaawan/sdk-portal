# Price Monthly 10

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTEw

Monthly costs for a Server type in this Location

*This model accepts additional fields of type object.*


# Class Name

`PriceMonthly10`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Gross` | `string` | Required | Price with VAT added |
| `Net` | `string` | Required | Price without VAT |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

PriceMonthly10 priceMonthly10 = new PriceMonthly10
{
    Gross = "1.1900000000000000",
    Net = "1.0000000000",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



