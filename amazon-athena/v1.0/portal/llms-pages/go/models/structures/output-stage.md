# Output Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRk91dHB1dFN0YWdl


# Class Name

`OutputStage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StageId` | `*int` | Optional | - |
| `State` | `*string` | Optional | - |
| `OutputBytes` | `*int` | Optional | - |
| `OutputRows` | `*int` | Optional | - |
| `InputBytes` | `*int` | Optional | - |
| `InputRows` | `*int` | Optional | - |
| `ExecutionTime` | `*int` | Optional | - |
| `QueryStagePlan` | [`*models.QueryStagePlan`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-stage-plan.md) | Optional | - |
| `SubStages` | [`[]models.QueryStage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-stage.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    outputStage := models.OutputStage{
        StageId:              models.ToPointer(26),
        State:                models.ToPointer("State4"),
        OutputBytes:          models.ToPointer(212),
        OutputRows:           models.ToPointer(54),
        InputBytes:           models.ToPointer(170),
    }

}
```



