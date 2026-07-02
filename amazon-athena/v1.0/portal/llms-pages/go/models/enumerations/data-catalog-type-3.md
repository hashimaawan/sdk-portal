# Data Catalog Type 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nVHlwZTM

Specifies the type of data catalog to update. Specify <code>LAMBDA</code> for a federated catalog, <code>HIVE</code> for an external hive metastore, or <code>GLUE</code> for an Glue Data Catalog.


# Class Name

`DataCatalogType3Enum`


# Fields

| Name |
|  --- |
| `LAMBDA` |
| `GLUE` |
| `HIVE` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    dataCatalogType3 := models.DataCatalogType3Enum_LAMBDA

}
```



