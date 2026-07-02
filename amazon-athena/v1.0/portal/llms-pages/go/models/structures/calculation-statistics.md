# Calculation Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdGlzdGljcw

Contains statistics for a notebook calculation.

*This model accepts additional fields of type interface{}.*


# Class Name

`CalculationStatistics`


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
    calculationStatistics := models.CalculationStatistics{
        DpuExecutionInMillis:  models.ToPointer(248),
        Progress:              models.ToPointer("Progress8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



