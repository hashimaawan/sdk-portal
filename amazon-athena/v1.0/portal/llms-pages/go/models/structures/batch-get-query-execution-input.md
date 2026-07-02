# Batch Get Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25JbnB1dA

Contains an array of query execution IDs.

*This model accepts additional fields of type interface{}.*


# Class Name

`BatchGetQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionIds` | `[]string` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    batchGetQueryExecutionInput := models.BatchGetQueryExecutionInput{
        QueryExecutionIds:     []string{
            "QueryExecutionIds7",
            "QueryExecutionIds8",
            "QueryExecutionIds9",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



