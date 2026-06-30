# Label Selector

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I


# Class Name

`LabelSelector`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Selector` | `string` | Required | Label selector |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    labelSelector := models.LabelSelector{
        Selector:             "env=prod",
    }

}
```



