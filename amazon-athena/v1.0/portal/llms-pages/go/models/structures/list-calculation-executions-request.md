# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0


# Class Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `StateFilter` | [`*models.CalculationExecutionState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/calculation-execution-state-3.md) | Optional | - |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `*string` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listCalculationExecutionsRequest := models.ListCalculationExecutionsRequest{
        SessionId:            "SessionId2",
        StateFilter:          models.ToPointer(models.CalculationExecutionState3Enum_QUEUED),
        MaxResults:           models.ToPointer(100),
        NextToken:            models.ToPointer("NextToken0"),
    }

}
```



