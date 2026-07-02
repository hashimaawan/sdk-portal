# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ

*This model accepts additional fields of type interface{}.*


# Class Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CalculationExecutionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `State` | [`*models.CalculationExecutionState4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/calculation-execution-state-4.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    startCalculationExecutionResponse := models.StartCalculationExecutionResponse{
        CalculationExecutionId: models.ToPointer("CalculationExecutionId0"),
        State:                  models.ToPointer(models.CalculationExecutionState4_Canceling),
        AdditionalProperties:   map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



