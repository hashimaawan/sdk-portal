# Result Set Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRhMg


# Class Name

`ResultSetMetadata2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ColumnInfo` | [`[]models.ColumnInfo`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/column-info.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    resultSetMetadata2 := models.ResultSetMetadata2{
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
    }

}
```



