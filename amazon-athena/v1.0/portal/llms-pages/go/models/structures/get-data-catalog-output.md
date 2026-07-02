# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DataCatalog` | [`*models.DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/data-catalog-2.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getDataCatalogOutput := models.GetDataCatalogOutput{
        DataCatalog:          models.ToPointer(models.DataCatalog2{
            Name:                 "Name4",
            Description:          models.ToPointer("Description2"),
            Type:                 models.DataCatalogType1Enum_GLUE,
            Parameters:           models.ToPointer(models.Parameters{
            }),
        }),
    }

}
```



