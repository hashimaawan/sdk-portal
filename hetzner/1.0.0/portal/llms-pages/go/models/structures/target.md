# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlRhcmdldA

*This model accepts additional fields of type interface{}.*


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HealthStatus` | [`[]models.HealthStatus`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/health-status.md) | Optional | - |
| `Server` | [`*models.Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-11.md) | Optional | - |
| `Type` | `*string` | Optional | - |
| `UsePrivateIp` | `*bool` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    target := models.Target{
        HealthStatus:          []models.HealthStatus{
            models.HealthStatus{
                ListenPort:            models.ToPointer(142),
                Status:                models.ToPointer(models.Status30_Unknown),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.HealthStatus{
                ListenPort:            models.ToPointer(142),
                Status:                models.ToPointer(models.Status30_Unknown),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.HealthStatus{
                ListenPort:            models.ToPointer(142),
                Status:                models.ToPointer(models.Status30_Unknown),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Server:                models.ToPointer(models.Server11{
            Id:                    14,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Type:                  models.ToPointer("server"),
        UsePrivateIp:          models.ToPointer(false),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



