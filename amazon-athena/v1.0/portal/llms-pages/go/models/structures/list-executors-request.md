# List Executors Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXF1ZXN0


# Class Name

`ListExecutorsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `ExecutorStateFilter` | [`*models.ExecutorState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/executor-state-1.md) | Optional | - |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `*string` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listExecutorsRequest := models.ListExecutorsRequest{
        SessionId:            "SessionId0",
        ExecutorStateFilter:  models.ToPointer(models.ExecutorState1Enum_CREATING),
        MaxResults:           models.ToPointer(100),
        NextToken:            models.ToPointer("NextToken8"),
    }

}
```



