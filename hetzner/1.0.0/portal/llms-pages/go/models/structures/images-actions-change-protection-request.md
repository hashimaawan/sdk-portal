# Images Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Class Name

`ImagesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `*bool` | Optional | If true, prevents the snapshot from being deleted |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    imagesActionsChangeProtectionRequest := models.ImagesActionsChangeProtectionRequest{
        Delete:               models.ToPointer(true),
    }

}
```



