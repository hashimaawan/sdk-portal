# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q


# Class Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New name to set |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    updateServerRequest := models.UpdateServerRequest{
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Name:                 models.ToPointer("my-server"),
    }

}
```



