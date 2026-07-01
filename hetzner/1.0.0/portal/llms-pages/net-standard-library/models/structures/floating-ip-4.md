# Floating Ip 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA0

The cost of one Floating IP per month

*This model accepts additional fields of type object.*


# Class Name

`FloatingIp4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PriceMonthly` | [`PriceMonthly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-monthly-6.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

FloatingIp4 floatingIp4 = new FloatingIp4
{
    PriceMonthly = new PriceMonthly6
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



