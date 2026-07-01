# Server 16

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcjE2

Configuration for type Server, required if type is `server`


# Class Name

`Server16`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `float64` | Required | ID of the Server |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    server16 := models.Server16{
        Id: float64(80),
    }

}
```



