# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1

*This model accepts additional fields of type object.*


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Prices` | [`List<Price6>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-6.md) | Required | Floating IP type costs per Location |
| `Type` | [`Type48`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-48.md) | Required | The type of the Floating IP |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

FloatingIp5 floatingIp5 = new FloatingIp5
{
    Prices = new List<Price6>
    {
        new Price6
        {
            Location = "fsn1",
            PriceMonthly = new PriceMonthly7
            {
                Gross = "1.1900000000000000",
                Net = "1.0000000000",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Type = Type48.Ipv4,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



