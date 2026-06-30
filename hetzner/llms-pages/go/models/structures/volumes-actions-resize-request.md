# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Size` | `float64` | Required | New Volume size in GB (must be greater than current size) |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    volumesActionsResizeRequest := models.VolumesActionsResizeRequest{
        Size:                 float64(50),
    }

}
```



