# Label Selector 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I1

Configuration for type label_selector, required if type is `label_selector`


# Class Name

`LabelSelector5`


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
    labelSelector5 := models.LabelSelector5{
        Selector:             "env=prod",
    }

}
```



