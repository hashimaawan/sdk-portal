# Labels 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkxhYmVsczI

User-defined labels (key-value pairs)


# Class Name

`Labels2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labelkey` | `*string` | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    labels2 := models.Labels2{
        Labelkey:             models.ToPointer("value"),
    }

}
```



