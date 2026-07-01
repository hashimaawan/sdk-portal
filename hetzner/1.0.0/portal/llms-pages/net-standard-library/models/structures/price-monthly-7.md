# Price Monthly 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTc

Monthly costs for a Floating IP type in this Location

*This model accepts additional fields of type object.*


# Class Name

`PriceMonthly7`


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

PriceMonthly7 priceMonthly7 = new PriceMonthly7
{
    Gross = "1.1900000000000000",
    Net = "1.0000000000",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



