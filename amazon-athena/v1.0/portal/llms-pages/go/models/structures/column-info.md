# Column Info

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNvbHVtbkluZm8

Information about the columns in a query execution result.

*This model accepts additional fields of type interface{}.*


# Class Name

`ColumnInfo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CatalogName` | `*string` | Optional | - |
| `SchemaName` | `*string` | Optional | - |
| `TableName` | `*string` | Optional | - |
| `Name` | `string` | Required | - |
| `Label` | `*string` | Optional | - |
| `Type` | `string` | Required | - |
| `Precision` | `*int` | Optional | - |
| `Scale` | `*int` | Optional | - |
| `Nullable` | [`*models.ColumnNullable2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/column-nullable-2.md) | Optional | - |
| `CaseSensitive` | `*bool` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    columnInfo := models.ColumnInfo{
        CatalogName:           models.ToPointer("CatalogName2"),
        SchemaName:            models.ToPointer("SchemaName2"),
        TableName:             models.ToPointer("TableName4"),
        Name:                  "Name8",
        Label:                 models.ToPointer("Label6"),
        Type:                  "Type8",
        Precision:             models.ToPointer(196),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



