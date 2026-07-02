# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0


# Class Name

`ListApplicationDPUSizesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplicationDPUSizes` | [`List<ApplicationDPUSizes>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/application-dpu-sizes.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

ListApplicationDPUSizesOutput listApplicationDPUSizesOutput = new ListApplicationDPUSizesOutput
{
    ApplicationDPUSizes = new List<ApplicationDPUSizes>
    {
        new ApplicationDPUSizes
        {
            ApplicationRuntimeId = "ApplicationRuntimeId0",
            SupportedDPUSizes = new List<int>
            {
                113,
                114,
            },
        },
        new ApplicationDPUSizes
        {
            ApplicationRuntimeId = "ApplicationRuntimeId0",
            SupportedDPUSizes = new List<int>
            {
                113,
                114,
            },
        },
    },
    NextToken = "NextToken0",
};
```



