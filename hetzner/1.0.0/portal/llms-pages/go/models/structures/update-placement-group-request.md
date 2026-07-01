# Update Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA


# Class Name

`UpdatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New PlacementGroup name |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    updatePlacementGroupRequest := models.UpdatePlacementGroupRequest{
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Name:                 models.ToPointer("my Placement Group"),
    }

}
```



