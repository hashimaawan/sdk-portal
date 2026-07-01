# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `*string` | Optional | New description of Image |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Type` | [`*models.Type24Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-24.md) | Optional | Destination Image type to convert to |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    updateImageRequest := models.UpdateImageRequest{
        Description:          models.ToPointer("My new Image description"),
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Type:                 models.ToPointer(models.Type24Enum_SNAPSHOT),
    }

}
```



