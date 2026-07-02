# Result Set Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRh

The metadata that describes the column structure and data types of a table of query results. To return a <code>ResultSetMetadata</code> object, use <a>GetQueryResults</a>.

*This model accepts additional fields of type interface{}.*


# Class Name

`ResultSetMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ColumnInfo` | [`[]models.ColumnInfo`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/column-info.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    resultSetMetadata := models.ResultSetMetadata{
        ColumnInfo:            []models.ColumnInfo{
            models.ColumnInfo{
                CatalogName:           models.ToPointer("CatalogName0"),
                SchemaName:            models.ToPointer("SchemaName0"),
                TableName:             models.ToPointer("TableName2"),
                Name:                  "Name6",
                Label:                 models.ToPointer("Label4"),
                Type:                  "Type6",
                Precision:             models.ToPointer(48),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.ColumnInfo{
                CatalogName:           models.ToPointer("CatalogName0"),
                SchemaName:            models.ToPointer("SchemaName0"),
                TableName:             models.ToPointer("TableName2"),
                Name:                  "Name6",
                Label:                 models.ToPointer("Label4"),
                Type:                  "Type6",
                Precision:             models.ToPointer(48),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



