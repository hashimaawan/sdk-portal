# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaWNlNw

*This model accepts additional fields of type object.*


# Class Name

`Price7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceHourly` | [`PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone |
| `PriceMonthly` | [`PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

Price7 price7 = new Price7
{
    Location = "fsn1",
    PriceHourly = new PriceHourly6
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    PriceMonthly = new PriceMonthly8
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



