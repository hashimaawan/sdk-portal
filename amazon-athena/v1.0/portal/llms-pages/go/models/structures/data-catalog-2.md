# Data Catalog 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nMg

*This model accepts additional fields of type interface{}.*


# Class Name

`DataCatalog2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `Type` | [`models.DataCatalogType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/data-catalog-type-1.md) | Required | - |
| `Parameters` | [`*models.Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/parameters.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    dataCatalog2 := models.DataCatalog2{
        Name:                  "Name6",
        Description:           models.ToPointer("Description0"),
        Type:                  models.DataCatalogType1_Lambda,
        Parameters:            models.ToPointer(models.Parameters{
            AdditionalProperties:  map[string]string{
                "exampleAdditionalProperty": "Parameters_additionalProperties2",
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



