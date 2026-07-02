# Unprocessed Query Execution Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUXVlcnlFeGVjdXRpb25JZA

Describes a query execution that failed to process.


# Class Name

`UnprocessedQueryExecutionId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `ErrorCode` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `ErrorMessage` | `*string` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    unprocessedQueryExecutionId := models.UnprocessedQueryExecutionId{
        QueryExecutionId:     models.ToPointer("QueryExecutionId6"),
        ErrorCode:            models.ToPointer("ErrorCode2"),
        ErrorMessage:         models.ToPointer("ErrorMessage8"),
    }

}
```



