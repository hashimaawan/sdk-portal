# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0

*This model accepts additional fields of type object.*


# Class Name

`ListApplicationDpuSizesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplicationDpuSizes` | [`List<ApplicationDpuSizes>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/application-dpu-sizes.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

ListApplicationDpuSizesOutput listApplicationDpuSizesOutput = new ListApplicationDpuSizesOutput
{
    ApplicationDpuSizes = new List<ApplicationDpuSizes>
    {
        new ApplicationDpuSizes
        {
            ApplicationRuntimeId = "ApplicationRuntimeId0",
            SupportedDpuSizes = new List<int>
            {
                113,
                114,
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ApplicationDpuSizes
        {
            ApplicationRuntimeId = "ApplicationRuntimeId0",
            SupportedDpuSizes = new List<int>
            {
                113,
                114,
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    NextToken = "NextToken0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



