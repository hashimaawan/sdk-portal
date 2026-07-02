# Get Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nSW5wdXQ


# Class Name

`GetDataCatalogInput`


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
    getDataCatalogInput := models.GetDataCatalogInput{
        Name:                 "Name6",
    }

}
```



