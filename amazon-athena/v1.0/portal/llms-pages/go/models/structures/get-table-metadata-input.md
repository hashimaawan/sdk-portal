# Get Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFJbnB1dA


# Class Name

`GetTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CatalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `DatabaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `TableName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getTableMetadataInput := models.GetTableMetadataInput{
        CatalogName:          "CatalogName2",
        DatabaseName:         "DatabaseName2",
        TableName:            "TableName4",
    }

}
```



