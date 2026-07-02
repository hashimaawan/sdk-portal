# Statistics 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mz

*This model accepts additional fields of type interface{}.*


# Class Name

`Statistics3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DpuExecutionInMillis` | `*int` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    statistics3 := models.Statistics3{
        DpuExecutionInMillis:  models.ToPointer(130),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



