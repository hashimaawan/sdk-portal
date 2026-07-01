# Labels

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxhYmVscw

User-defined labels (key-value pairs)


# Class Name

`Labels`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labelkey` | `*string` | Optional | New label |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    labels := models.Labels{
        Labelkey:             models.ToPointer("value"),
    }

}
```



