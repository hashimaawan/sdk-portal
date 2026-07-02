# Result Set 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdFNldDI


# Class Name

`ResultSet2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Rows` | [`[]models.Row`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/row.md) | Optional | - |
| `ResultSetMetadata` | [`*models.ResultSetMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-set-metadata-2.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    resultSet2 := models.ResultSet2{
        Rows:                 []models.Row{
            models.Row{
                Data:                 []models.Datum{
                    models.Datum{
                        VarCharValue:         models.ToPointer("VarCharValue8"),
                    },
                    models.Datum{
                        VarCharValue:         models.ToPointer("VarCharValue8"),
                    },
                },
            },
        },
        ResultSetMetadata:    models.ToPointer(models.ResultSetMetadata2{
            ColumnInfo:           []models.ColumnInfo{
                models.ColumnInfo{
                    CatalogName:          models.ToPointer("CatalogName0"),
                    SchemaName:           models.ToPointer("SchemaName0"),
                    TableName:            models.ToPointer("TableName2"),
                    Name:                 "Name6",
                    Label:                models.ToPointer("Label4"),
                    Type:                 "Type6",
                    Precision:            models.ToPointer(48),
                },
            },
        }),
    }

}
```



