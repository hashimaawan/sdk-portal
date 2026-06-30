# Update Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlVwZGF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Class Name

`UpdateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `*string` | Optional | New Description to set |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New unique name to set |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    updateFloatingIPRequest := models.UpdateFloatingIPRequest{
        Description:          models.ToPointer("Web Frontend"),
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Name:                 models.ToPointer("Web Frontend"),
    }

}
```



