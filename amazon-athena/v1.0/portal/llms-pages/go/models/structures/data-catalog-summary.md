# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.

*This model accepts additional fields of type interface{}.*


# Class Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CatalogName` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Type` | [`*models.DataCatalogType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/data-catalog-type-2.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    dataCatalogSummary := models.DataCatalogSummary{
        CatalogName:           models.ToPointer("CatalogName2"),
        Type:                  models.ToPointer(models.DataCatalogType2_Hive),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



