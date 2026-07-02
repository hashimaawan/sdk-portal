# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0

*This model accepts additional fields of type interface{}.*


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DataCatalog` | [`*models.DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/data-catalog-2.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    getDataCatalogOutput := models.GetDataCatalogOutput{
        DataCatalog:           models.ToPointer(models.DataCatalog2{
            Name:                  "Name4",
            Description:           models.ToPointer("Description2"),
            Type:                  models.DataCatalogType1_Glue,
            Parameters:            models.ToPointer(models.Parameters{
                AdditionalProperties:  map[string]string{
                    "exampleAdditionalProperty": "Parameters_additionalProperties2",
                },
            }),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



