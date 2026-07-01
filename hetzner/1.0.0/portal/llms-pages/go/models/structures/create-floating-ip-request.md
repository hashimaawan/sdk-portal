# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Class Name

`CreateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `*string` | Optional | - |
| `HomeLocation` | `*string` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | - |
| `Server` | `*int` | Optional | Server to assign the Floating IP to |
| `Type` | [`models.Type17Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-17.md) | Required | Floating IP type |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createFloatingIPRequest := models.CreateFloatingIPRequest{
        Description:          models.ToPointer("Web Frontend"),
        HomeLocation:         models.ToPointer("fsn1"),
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Name:                 models.ToPointer("Web Frontend"),
        Server:               models.ToPointer(42),
        Type:                 models.Type17Enum_IPV4,
    }

}
```



