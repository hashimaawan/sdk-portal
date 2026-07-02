# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0

*This model accepts additional fields of type interface{}.*


# Class Name

`ListApplicationDpuSizesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplicationDpuSizes` | [`[]models.ApplicationDpuSizes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/application-dpu-sizes.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listApplicationDpuSizesOutput := models.ListApplicationDpuSizesOutput{
        ApplicationDpuSizes:   []models.ApplicationDpuSizes{
            models.ApplicationDpuSizes{
                ApplicationRuntimeId:  models.ToPointer("ApplicationRuntimeId0"),
                SupportedDpuSizes:     []int{
                    113,
                    114,
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.ApplicationDpuSizes{
                ApplicationRuntimeId:  models.ToPointer("ApplicationRuntimeId0"),
                SupportedDpuSizes:     []int{
                    113,
                    114,
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        NextToken:             models.ToPointer("NextToken0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



