# Row

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJvdw

The rows that make up a query result table.


# Class Name

`Row`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | [`[]models.Datum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/datum.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    row := models.Row{
        Data:                 []models.Datum{
            models.Datum{
                VarCharValue:         models.ToPointer("VarCharValue8"),
            },
        },
    }

}
```



