# State

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXRl

A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`.


# Class Name

`State`


# Fields

| Name |
|  --- |
| `Pending` |
| `Verified` |
| `EnumError` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    state := models.State_EnumError

}
```



