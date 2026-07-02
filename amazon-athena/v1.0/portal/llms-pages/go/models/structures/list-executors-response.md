# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ


# Class Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `NextToken` | `*string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `ExecutorsSummary` | [`[]models.ExecutorsSummary`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/executors-summary.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listExecutorsResponse := models.ListExecutorsResponse{
        SessionId:            "SessionId4",
        NextToken:            models.ToPointer("NextToken4"),
        ExecutorsSummary:     []models.ExecutorsSummary{
            models.ExecutorsSummary{
                ExecutorId:           "ExecutorId8",
                ExecutorType:         models.ToPointer(models.ExecutorType2Enum_GATEWAY),
                StartDateTime:        models.ToPointer(128),
                TerminationDateTime:  models.ToPointer(236),
                ExecutorState:        models.ToPointer(models.ExecutorState3Enum_TERMINATED),
                ExecutorSize:         models.ToPointer(42),
            },
            models.ExecutorsSummary{
                ExecutorId:           "ExecutorId8",
                ExecutorType:         models.ToPointer(models.ExecutorType2Enum_GATEWAY),
                StartDateTime:        models.ToPointer(128),
                TerminationDateTime:  models.ToPointer(236),
                ExecutorState:        models.ToPointer(models.ExecutorState3Enum_TERMINATED),
                ExecutorSize:         models.ToPointer(42),
            },
            models.ExecutorsSummary{
                ExecutorId:           "ExecutorId8",
                ExecutorType:         models.ToPointer(models.ExecutorType2Enum_GATEWAY),
                StartDateTime:        models.ToPointer(128),
                TerminationDateTime:  models.ToPointer(236),
                ExecutorState:        models.ToPointer(models.ExecutorState3Enum_TERMINATED),
                ExecutorSize:         models.ToPointer(42),
            },
        },
    }

}
```



