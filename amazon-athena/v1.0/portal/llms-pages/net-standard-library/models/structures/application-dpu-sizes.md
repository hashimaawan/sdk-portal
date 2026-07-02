# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.


# Class Name

`ApplicationDPUSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplicationRuntimeId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `SupportedDPUSizes` | `List<int>` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

ApplicationDPUSizes applicationDPUSizes = new ApplicationDPUSizes
{
    ApplicationRuntimeId = "ApplicationRuntimeId2",
    SupportedDPUSizes = new List<int>
    {
        57,
    },
};
```



