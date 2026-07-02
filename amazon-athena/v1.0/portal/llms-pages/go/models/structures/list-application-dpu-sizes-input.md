# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ListApplicationDpuSizesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listApplicationDpuSizesInput := models.ListApplicationDpuSizesInput{
        MaxResults:            models.ToPointer(56),
        NextToken:             models.ToPointer("NextToken6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



