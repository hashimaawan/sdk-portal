# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | [`*models.Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New network name |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    updateNetworkRequest := models.UpdateNetworkRequest{
        Labels:               models.ToPointer(models.Labels2{
            Labelkey:             models.ToPointer("labelkey4"),
        }),
        Name:                 models.ToPointer("new-name"),
    }

}
```



