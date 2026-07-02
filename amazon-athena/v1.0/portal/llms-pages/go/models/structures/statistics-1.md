# Statistics 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mx

*This model accepts additional fields of type interface{}.*


# Class Name

`Statistics1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DpuExecutionInMillis` | `*int` | Optional | - |
| `Progress` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    statistics1 := models.Statistics1{
        DpuExecutionInMillis:  models.ToPointer(148),
        Progress:              models.ToPointer("Progress4"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



