# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.

*This model accepts additional fields of type object.*


# Class Name

`ApplicationDpuSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplicationRuntimeId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `SupportedDpuSizes` | `List<int>` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

ApplicationDpuSizes applicationDpuSizes = new ApplicationDpuSizes
{
    ApplicationRuntimeId = "ApplicationRuntimeId4",
    SupportedDpuSizes = new List<int>
    {
        17,
        18,
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



