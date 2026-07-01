# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByaW1hcnlJcA

*This model accepts additional fields of type object.*


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Prices` | [`List<Price8>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price-8.md) | Required | Primary IP type costs per Location |
| `Type` | [`Type49`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-49.md) | Required | The type of the Primary IP |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

PrimaryIp primaryIp = new PrimaryIp
{
    Prices = new List<Price8>
    {
        new Price8
        {
            Location = "fsn1",
            PriceHourly = new PriceHourly7
            {
                Gross = "1.1900000000000000",
                Net = "1.0000000000",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            PriceMonthly = new PriceMonthly9
            {
                Gross = "1.1900000000000000",
                Net = "1.0000000000",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Type = Type49.Ipv4,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



