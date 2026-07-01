# Image 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlMw

The cost of Image per GB/month

*This model accepts additional fields of type object.*


# Class Name

`Image3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-per-gb-month.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

Image3 image3 = new Image3
{
    PricePerGbMonth = new PricePerGbMonth
    {
        Gross = "1.1900000000000000",
        Net = "1.0000000000",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



