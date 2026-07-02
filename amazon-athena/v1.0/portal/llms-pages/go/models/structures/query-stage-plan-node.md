# Query Stage Plan Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFuTm9kZQ

Stage plan information such as name, identifier, sub plans, and remote sources.


# Class Name

`QueryStagePlanNode`


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
    queryStagePlanNode := models.QueryStagePlanNode{
        Name:                 models.ToPointer("Name4"),
        Identifier:           models.ToPointer("Identifier0"),
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
            "RemoteSources2",
            "RemoteSources3",
            "RemoteSources4",
        },
    }

}
```



