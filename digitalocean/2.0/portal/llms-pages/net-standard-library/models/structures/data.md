# Data

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGE

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Data`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Result` | [`List<Result>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/result.md) | Required | Result of query. |
| `ResultType` | `string` | Required, Constant | **Value**: `"matrix"` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Data data = new Data
{
    Result = new List<Result>
    {
        new Result
        {
            Metric = new Dictionary<string, string>
            {
                ["host_id"] = "19201920",
            },
            Values = new List<List<ResultValues>>
            {
                new List<ResultValues>
                {
                    ResultValues.FromNumber(1435781430),
                    ResultValues.FromString("1"),
                },
                new List<ResultValues>
                {
                    ResultValues.FromNumber(1435781445),
                    ResultValues.FromString("1"),
                },
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ResultType = "matrix",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



