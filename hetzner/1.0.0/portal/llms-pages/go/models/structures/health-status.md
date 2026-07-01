# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ListenPort` | `*int` | Optional | - |
| `Status` | [`*models.Status30Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/status-30.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    healthStatus := models.HealthStatus{
        ListenPort:           models.ToPointer(443),
        Status:               models.ToPointer(models.Status30Enum_HEALTHY),
    }

}
```



