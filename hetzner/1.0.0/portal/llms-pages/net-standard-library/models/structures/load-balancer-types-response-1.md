# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancerType` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-type.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

LoadBalancerTypesResponse1 loadBalancerTypesResponse1 = new LoadBalancerTypesResponse1
{
    LoadBalancerType = new LoadBalancerType
    {
        Deprecated = "deprecated2",
        Description = "description4",
        Id = 205.06,
        MaxAssignedCertificates = 211.64,
        MaxConnections = 136.32,
        MaxServices = 199.18,
        MaxTargets = 152.52,
        Name = "name6",
        Prices = new List<Price>
        {
            new Price
            {
                Location = "location8",
                PriceHourly = new PriceHourly
                {
                    Gross = "gross4",
                    Net = "net2",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                PriceMonthly = new PriceMonthly
                {
                    Gross = "gross2",
                    Net = "net0",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Price
            {
                Location = "location8",
                PriceHourly = new PriceHourly
                {
                    Gross = "gross4",
                    Net = "net2",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                PriceMonthly = new PriceMonthly
                {
                    Gross = "gross2",
                    Net = "net0",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Price
            {
                Location = "location8",
                PriceHourly = new PriceHourly
                {
                    Gross = "gross4",
                    Net = "net2",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                PriceMonthly = new PriceMonthly
                {
                    Gross = "gross2",
                    Net = "net0",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



