# Query Execution Context 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dDE


# Class Name

`QueryExecutionContext1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `Catalog` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    queryExecutionContext1 := models.QueryExecutionContext1{
        Database:             models.ToPointer("Database0"),
        Catalog:              models.ToPointer("Catalog6"),
    }

}
```



