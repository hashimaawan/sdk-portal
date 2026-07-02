# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.

*This model accepts additional fields of type interface{}.*


# Class Name

`ApplicationDpuSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplicationRuntimeId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `SupportedDpuSizes` | `[]int` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    applicationDpuSizes := models.ApplicationDpuSizes{
        ApplicationRuntimeId:  models.ToPointer("ApplicationRuntimeId4"),
        SupportedDpuSizes:     []int{
            17,
            18,
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



