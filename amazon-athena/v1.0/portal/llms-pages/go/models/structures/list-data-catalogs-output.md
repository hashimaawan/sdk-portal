# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DataCatalogsSummary` | [`[]models.DataCatalogSummary`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/data-catalog-summary.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listDataCatalogsOutput := models.ListDataCatalogsOutput{
        DataCatalogsSummary:  []models.DataCatalogSummary{
            models.DataCatalogSummary{
                CatalogName:          models.ToPointer("CatalogName4"),
                Type:                 models.ToPointer(models.DataCatalogType2Enum_HIVE),
            },
            models.DataCatalogSummary{
                CatalogName:          models.ToPointer("CatalogName4"),
                Type:                 models.ToPointer(models.DataCatalogType2Enum_HIVE),
            },
            models.DataCatalogSummary{
                CatalogName:          models.ToPointer("CatalogName4"),
                Type:                 models.ToPointer(models.DataCatalogType2Enum_HIVE),
            },
        },
        NextToken:            models.ToPointer("NextToken0"),
    }

}
```



