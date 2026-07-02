# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.


# Class Name

`ApplicationDPUSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplicationRuntimeId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `SupportedDPUSizes` | `[]int` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    applicationDPUSizes := models.ApplicationDPUSizes{
        ApplicationRuntimeId: models.ToPointer("ApplicationRuntimeId2"),
        SupportedDPUSizes:    []int{
            57,
        },
    }

}
```



