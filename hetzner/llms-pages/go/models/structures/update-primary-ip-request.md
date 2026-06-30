# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q


# Class Name

`UpdatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutoDelete` | `*bool` | Optional | Delete this Primary IP when the resource it is assigned to is deleted |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New unique name to set |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    updatePrimaryIPRequest := models.UpdatePrimaryIPRequest{
        AutoDelete:           models.ToPointer(true),
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Name:                 models.ToPointer("my-ip"),
    }

}
```



