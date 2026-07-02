# Get Database Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldERhdGFiYXNlSW5wdXQ


# Class Name

`GetDatabaseInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CatalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `DatabaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getDatabaseInput := models.GetDatabaseInput{
        CatalogName:          "CatalogName2",
        DatabaseName:         "DatabaseName2",
    }

}
```



