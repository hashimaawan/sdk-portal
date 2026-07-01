# Price Monthly 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTk

Monthly costs for a Primary IP type in this Location

*This model accepts additional fields of type object.*


# Class Name

`PriceMonthly9`


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

PriceMonthly9 priceMonthly9 = new PriceMonthly9
{
    Gross = "1.1900000000000000",
    Net = "1.0000000000",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



