# Load Balancer Type 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU2

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancerType6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `double` | Required | ID of the Load Balancer type the price is for |
| `Name` | `string` | Required | Name of the Load Balancer type the price is for |
| `Prices` | [`List<Price7>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-7.md) | Required | Load Balancer type costs per Location |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

LoadBalancerType6 loadBalancerType6 = new LoadBalancerType6
{
    Id = 1,
    Name = "lb11",
    Prices = new List<Price7>
    {
        new Price7
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
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



