# Query Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2U

Stage statistics such as input and output rows and bytes, execution time and stage state. This information also includes substages and the query stage plan.


# Class Name

`QueryStage`


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
    queryStage := models.QueryStage{
        StageId:              models.ToPointer(118),
        State:                models.ToPointer("State0"),
        OutputBytes:          models.ToPointer(120),
        OutputRows:           models.ToPointer(146),
        InputBytes:           models.ToPointer(178),
    }

}
```



