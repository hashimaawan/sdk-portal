# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ


# Class Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CalculationExecutionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `State` | [`*models.CalculationExecutionState4Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/calculation-execution-state-4.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    startCalculationExecutionResponse := models.StartCalculationExecutionResponse{
        CalculationExecutionId: models.ToPointer("CalculationExecutionId0"),
        State:                  models.ToPointer(models.CalculationExecutionState4Enum_CANCELING),
    }

}
```



