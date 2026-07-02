# Unprocessed Query Execution Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUXVlcnlFeGVjdXRpb25JZA

Describes a query execution that failed to process.

*This model accepts additional fields of type interface{}.*


# Class Name

`UnprocessedQueryExecutionId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `ErrorCode` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `ErrorMessage` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    unprocessedQueryExecutionId := models.UnprocessedQueryExecutionId{
        QueryExecutionId:      models.ToPointer("QueryExecutionId6"),
        ErrorCode:             models.ToPointer("ErrorCode2"),
        ErrorMessage:          models.ToPointer("ErrorMessage8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



