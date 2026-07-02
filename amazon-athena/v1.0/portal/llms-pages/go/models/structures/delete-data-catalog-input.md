# Delete Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkRlbGV0ZURhdGFDYXRhbG9nSW5wdXQ


# Class Name

`DeleteDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    deleteDataCatalogInput := models.DeleteDataCatalogInput{
        Name:                 "Name2",
    }

}
```



