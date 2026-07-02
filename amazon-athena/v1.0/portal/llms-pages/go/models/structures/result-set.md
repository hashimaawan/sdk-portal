# Result Set

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdFNldA

The metadata and rows that make up a query result set. The metadata describes the column structure and data types. To return a <code>ResultSet</code> object, use <a>GetQueryResults</a>.


# Class Name

`ResultSet`


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
    resultSet := models.ResultSet{
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



