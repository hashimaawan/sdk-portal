# Create Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZURhdGFDYXRhbG9nSW5wdXQ


# Class Name

`CreateDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Type` | [`models.DataCatalogType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/data-catalog-type-1.md) | Required | - |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `Parameters` | [`*models.Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/parameters.md) | Optional | - |
| `Tags` | [`[]models.Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/tag.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    createDataCatalogInput := models.CreateDataCatalogInput{
        Name:                 "Name6",
        Type:                 models.DataCatalogType1Enum_GLUE,
        Description:          models.ToPointer("Description2"),
        Parameters:           models.ToPointer(models.Parameters{
        }),
        Tags:                 []models.Tag{
            models.Tag{
                Key:                  models.ToPointer("Key0"),
                Value:                models.ToPointer("Value6"),
            },
            models.Tag{
                Key:                  models.ToPointer("Key0"),
                Value:                models.ToPointer("Value6"),
            },
            models.Tag{
                Key:                  models.ToPointer("Key0"),
                Value:                models.ToPointer("Value6"),
            },
        },
    }

}
```



