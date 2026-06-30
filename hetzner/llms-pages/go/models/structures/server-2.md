# Server 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNlcnZlcjI

Configuration for type Server, required if type is `server`


# Class Name

`Server2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    server2 := models.Server2{
        Id:                   162,
    }

}
```



