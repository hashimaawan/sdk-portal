# Load Balancer Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldA

*This model accepts additional fields of type interface{}.*


# Class Name

`LoadBalancerTarget`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HealthStatus` | [`[]models.HealthStatus`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/health-status.md) | Optional | List of health statuses of the services on this target |
| `Ip` | [`*models.Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `LabelSelector` | [`*models.LabelSelector7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/label-selector-7.md) | Optional | Label selector and a list of selected targets |
| `Server` | [`*models.LoadBalancerTargetServer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/load-balancer-target-server.md) | Optional | Server where the traffic should be routed through |
| `Targets` | [`[]models.Target`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/target.md) | Optional | List of selected targets |
| `Type` | [`models.Type29`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-29.md) | Required | Type of the resource |
| `UsePrivateIp` | `*bool` | Optional | Use the private network IP instead of the public IP. Default value is false. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    loadBalancerTarget := models.LoadBalancerTarget{
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
        },
        Ip:                    models.ToPointer(models.Ip{
            Ip:                    "ip8",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        LabelSelector:         models.ToPointer(models.LabelSelector7{
            Selector:              "selector8",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Server:                models.ToPointer(models.LoadBalancerTargetServer{
            Id:                    14,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Targets:               []models.Target{
            models.Target{
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
                },
                Server:                models.ToPointer(models.Server11{
                    Id:                    14,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Type:                  models.ToPointer("type2"),
                UsePrivateIp:          models.ToPointer(false),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Target{
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
                },
                Server:                models.ToPointer(models.Server11{
                    Id:                    14,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Type:                  models.ToPointer("type2"),
                UsePrivateIp:          models.ToPointer(false),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Target{
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
                },
                Server:                models.ToPointer(models.Server11{
                    Id:                    14,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Type:                  models.ToPointer("type2"),
                UsePrivateIp:          models.ToPointer(false),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Type:                  models.Type29_LabelSelector,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



