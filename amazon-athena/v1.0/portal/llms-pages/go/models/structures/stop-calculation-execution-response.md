# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl


# Class Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `State` | [`*models.CalculationExecutionState4Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/calculation-execution-state-4.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    stopCalculationExecutionResponse := models.StopCalculationExecutionResponse{
        State:                models.ToPointer(models.CalculationExecutionState4Enum_QUEUED),
    }

}
```



