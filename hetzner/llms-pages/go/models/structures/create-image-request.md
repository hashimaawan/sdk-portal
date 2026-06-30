# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `*string` | Optional | Description of the Image, will be auto-generated if not set |
| `Labels` | [`*models.Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `Type` | [`*models.Type63Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createImageRequest := models.CreateImageRequest{
        Description:          models.ToPointer("my image"),
        Labels:               models.ToPointer(models.Labels{
            Labelkey:             models.ToPointer("labelkey4"),
        }),
        Type:                 models.ToPointer(models.Type63Enum_SNAPSHOT),
    }

}
```



