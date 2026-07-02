# Batch Get Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRJbnB1dA


# Class Name

`BatchGetPreparedStatementInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PreparedStatementNames` | `[]string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    batchGetPreparedStatementInput := models.BatchGetPreparedStatementInput{
        PreparedStatementNames: []string{
            "PreparedStatementNames8",
            "PreparedStatementNames9",
            "PreparedStatementNames0",
        },
        WorkGroup:              "WorkGroup6",
    }

}
```



