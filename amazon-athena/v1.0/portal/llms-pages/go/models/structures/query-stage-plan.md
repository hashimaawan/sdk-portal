# Query Stage Plan

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFu


# Class Name

`QueryStagePlan`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `*string` | Optional | - |
| `Identifier` | `*string` | Optional | - |
| `Children` | [`[]models.QueryStagePlanNode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-stage-plan-node.md) | Optional | - |
| `RemoteSources` | `[]string` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    queryStagePlan := models.QueryStagePlan{
        Name:                 models.ToPointer("Name0"),
        Identifier:           models.ToPointer("Identifier6"),
        Children:             []models.QueryStagePlanNode{
            models.QueryStagePlanNode{
                Name:                 models.ToPointer("Name6"),
                Identifier:           models.ToPointer("Identifier2"),
                Children:             []models.QueryStagePlanNode{
                    models.QueryStagePlanNode{
                    },
                },
                RemoteSources:        []string{
                    "RemoteSources4",
                    "RemoteSources5",
                    "RemoteSources6",
                },
            },
        },
        RemoteSources:        []string{
            "RemoteSources8",
            "RemoteSources9",
            "RemoteSources0",
        },
    }

}
```



