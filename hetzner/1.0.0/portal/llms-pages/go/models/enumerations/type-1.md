# Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlR5cGUx

Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`.


# Class Name

`Type1`


# Fields

| Name |
|  --- |
| `Uploaded` |
| `Managed` |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    type1 := models.Type1_Uploaded

}
```



