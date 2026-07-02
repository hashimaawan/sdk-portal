# Update Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZURhdGFDYXRhbG9nSW5wdXQ


# Class Name

`UpdateDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Type` | [`models.DataCatalogType3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/data-catalog-type-3.md) | Required | - |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `Parameters` | [`*models.Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/parameters.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    updateDataCatalogInput := models.UpdateDataCatalogInput{
        Name:                 "Name4",
        Type:                 models.DataCatalogType3Enum_GLUE,
        Description:          models.ToPointer("Description2"),
        Parameters:           models.ToPointer(models.Parameters{
        }),
    }

}
```



