# Data Catalog Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nVHlwZTE

The type of data catalog to create: <code>LAMBDA</code> for a federated catalog, <code>HIVE</code> for an external hive metastore, or <code>GLUE</code> for an Glue Data Catalog.


# Class Name

`DataCatalogType1`


# Fields

| Name |
|  --- |
| `Lambda` |
| `Glue` |
| `Hive` |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    dataCatalogType1 := models.DataCatalogType1_Glue

}
```



