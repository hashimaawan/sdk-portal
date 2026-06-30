# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ip` | `*string` | Optional | - |
| `Network` | `*int` | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    privateNet := models.PrivateNet{
        Ip:                   models.ToPointer("10.0.0.2"),
        Network:              models.ToPointer(4711),
    }

}
```



