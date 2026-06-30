# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA


# Class Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Network` | `int` | Required | ID of an existing network to detach the Server from |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    detachFromNetworkRequest := models.DetachFromNetworkRequest{
        Network:              4711,
    }

}
```



