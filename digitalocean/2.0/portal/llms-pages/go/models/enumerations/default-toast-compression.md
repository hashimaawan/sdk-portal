# Default Toast Compression

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRlZmF1bHRUb2FzdENvbXByZXNzaW9u

Specifies the default TOAST compression method for values of compressible columns (the default is lz4).


# Class Name

`DefaultToastCompression`


# Fields

| Name |
|  --- |
| `Lz4` |
| `Pglz` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    defaultToastCompression := models.DefaultToastCompression_Lz4

}
```



