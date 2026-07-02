# Output Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRk91dHB1dFN0YWdl

*This model accepts additional fields of type interface{}.*


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
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    outputStage := models.OutputStage{
        StageId:               models.ToPointer(26),
        State:                 models.ToPointer("State4"),
        OutputBytes:           models.ToPointer(212),
        OutputRows:            models.ToPointer(54),
        InputBytes:            models.ToPointer(170),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



