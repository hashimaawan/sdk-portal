# Type 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlR5cGU0

A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt.


# Class Name

`Type4`


# Fields

| Name |
|  --- |
| `Custom` |
| `LetsEncrypt` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    type4 := models.Type4_Custom

}
```



