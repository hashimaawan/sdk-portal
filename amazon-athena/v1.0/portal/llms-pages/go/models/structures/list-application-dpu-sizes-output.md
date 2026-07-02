# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0


# Class Name

`ListApplicationDPUSizesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplicationDPUSizes` | [`[]models.ApplicationDPUSizes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/application-dpu-sizes.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listApplicationDPUSizesOutput := models.ListApplicationDPUSizesOutput{
        ApplicationDPUSizes:  []models.ApplicationDPUSizes{
            models.ApplicationDPUSizes{
                ApplicationRuntimeId: models.ToPointer("ApplicationRuntimeId0"),
                SupportedDPUSizes:    []int{
                    113,
                    114,
                },
            },
            models.ApplicationDPUSizes{
                ApplicationRuntimeId: models.ToPointer("ApplicationRuntimeId0"),
                SupportedDPUSizes:    []int{
                    113,
                    114,
                },
            },
        },
        NextToken:            models.ToPointer("NextToken0"),
    }

}
```



