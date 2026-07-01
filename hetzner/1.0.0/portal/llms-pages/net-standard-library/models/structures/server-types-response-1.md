# Server Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type object.*


# Class Name

`ServerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerType` | [`ServerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-type.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

ServerTypesResponse1 serverTypesResponse1 = new ServerTypesResponse1
{
    ServerType = new ServerType
    {
        Cores = 1,
        CpuType = CpuType.Shared,
        Deprecated = false,
        Description = "CX11",
        Disk = 24,
        Id = 1,
        Memory = 1,
        Name = "cx11",
        Prices = new List<Price9>
        {
            new Price9
            {
                Location = "fsn1",
                PriceHourly = new PriceHourly8
                {
                    Gross = "1.1900000000000000",
                    Net = "1.0000000000",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                PriceMonthly = new PriceMonthly10
                {
                    Gross = "1.1900000000000000",
                    Net = "1.0000000000",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        StorageType = StorageType.Local,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



