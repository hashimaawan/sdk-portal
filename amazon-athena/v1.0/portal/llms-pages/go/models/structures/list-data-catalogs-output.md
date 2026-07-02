# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DataCatalogsSummary` | [`[]models.DataCatalogSummary`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/data-catalog-summary.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listDataCatalogsOutput := models.ListDataCatalogsOutput{
        DataCatalogsSummary:   []models.DataCatalogSummary{
            models.DataCatalogSummary{
                CatalogName:           models.ToPointer("CatalogName4"),
                Type:                  models.ToPointer(models.DataCatalogType2_Hive),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.DataCatalogSummary{
                CatalogName:           models.ToPointer("CatalogName4"),
                Type:                  models.ToPointer(models.DataCatalogType2_Hive),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.DataCatalogSummary{
                CatalogName:           models.ToPointer("CatalogName4"),
                Type:                  models.ToPointer(models.DataCatalogType2_Hive),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        NextToken:             models.ToPointer("NextToken0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



