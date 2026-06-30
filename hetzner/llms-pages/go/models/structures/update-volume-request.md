# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q


# Class Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | [`*models.Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | New Volume name |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    updateVolumeRequest := models.UpdateVolumeRequest{
        Labels:               models.ToPointer(models.Labels2{
            Labelkey:             models.ToPointer("labelkey4"),
        }),
        Name:                 "database-storage",
    }

}
```



