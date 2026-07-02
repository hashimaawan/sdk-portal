# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExecutorId` | `string` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` |
| `ExecutorType` | [`*models.ExecutorType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/executor-type-2.md) | Optional | - |
| `StartDateTime` | `*int` | Optional | - |
| `TerminationDateTime` | `*int` | Optional | - |
| `ExecutorState` | [`*models.ExecutorState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/executor-state-3.md) | Optional | - |
| `ExecutorSize` | `*int` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    executorsSummary := models.ExecutorsSummary{
        ExecutorId:           "ExecutorId8",
        ExecutorType:         models.ToPointer(models.ExecutorType2Enum_WORKER),
        StartDateTime:        models.ToPointer(52),
        TerminationDateTime:  models.ToPointer(56),
        ExecutorState:        models.ToPointer(models.ExecutorState3Enum_CREATING),
        ExecutorSize:         models.ToPointer(222),
    }

}
```



