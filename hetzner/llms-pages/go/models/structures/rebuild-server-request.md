# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Image` | `string` | Required | ID or name of Image to rebuilt from. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    rebuildServerRequest := models.RebuildServerRequest{
        Image:                "ubuntu-20.04",
    }

}
```



