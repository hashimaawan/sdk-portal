# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlRhcmdldA


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HealthStatus` | [`[]models.HealthStatus`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/health-status.md) | Optional | - |
| `Server` | [`*models.Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-11.md) | Optional | - |
| `Type` | `*string` | Optional | - |
| `UsePrivateIp` | `*bool` | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    target := models.Target{
        HealthStatus:         []models.HealthStatus{
            models.HealthStatus{
                ListenPort:           models.ToPointer(142),
                Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
            },
            models.HealthStatus{
                ListenPort:           models.ToPointer(142),
                Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
            },
            models.HealthStatus{
                ListenPort:           models.ToPointer(142),
                Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
            },
        },
        Server:               models.ToPointer(models.Server11{
            Id:                   14,
        }),
        Type:                 models.ToPointer("server"),
        UsePrivateIp:         models.ToPointer(false),
    }

}
```



