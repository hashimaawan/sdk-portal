# Get Query Results Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c091dHB1dA


# Class Name

`GetQueryResultsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `UpdateCount` | `*int` | Optional | - |
| `ResultSet` | [`*models.ResultSet2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-set-2.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getQueryResultsOutput := models.GetQueryResultsOutput{
        UpdateCount:          models.ToPointer(60),
        ResultSet:            models.ToPointer(models.ResultSet2{
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
        }),
        NextToken:            models.ToPointer("NextToken0"),
    }

}
```



