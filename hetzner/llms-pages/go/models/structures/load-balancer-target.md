# Load Balancer Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldA


# Class Name

`LoadBalancerTarget`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HealthStatus` | [`[]models.HealthStatus`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/health-status.md) | Optional | List of health statuses of the services on this target |
| `Ip` | [`*models.Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `LabelSelector` | [`*models.LabelSelector7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/label-selector-7.md) | Optional | Label selector and a list of selected targets |
| `Server` | [`*models.LoadBalancerTargetServer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/load-balancer-target-server.md) | Optional | Server where the traffic should be routed through |
| `Targets` | [`[]models.Target`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/target.md) | Optional | List of selected targets |
| `Type` | [`models.Type29Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-29.md) | Required | Type of the resource |
| `UsePrivateIp` | `*bool` | Optional | Use the private network IP instead of the public IP. Default value is false. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerTarget := models.LoadBalancerTarget{
        HealthStatus:         []models.HealthStatus{
            models.HealthStatus{
                ListenPort:           models.ToPointer(142),
                Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
            },
            models.HealthStatus{
                ListenPort:           models.ToPointer(142),
                Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
            },
        },
        Ip:                   models.ToPointer(models.Ip{
            Ip:                   "ip8",
        }),
        LabelSelector:        models.ToPointer(models.LabelSelector7{
            Selector:             "selector8",
        }),
        Server:               models.ToPointer(models.LoadBalancerTargetServer{
            Id:                   14,
        }),
        Targets:              []models.Target{
            models.Target{
                HealthStatus:         []models.HealthStatus{
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
                Type:                 models.ToPointer("type2"),
                UsePrivateIp:         models.ToPointer(false),
            },
            models.Target{
                HealthStatus:         []models.HealthStatus{
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
                Type:                 models.ToPointer("type2"),
                UsePrivateIp:         models.ToPointer(false),
            },
            models.Target{
                HealthStatus:         []models.HealthStatus{
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
                Type:                 models.ToPointer("type2"),
                UsePrivateIp:         models.ToPointer(false),
            },
        },
        Type:                 models.Type29Enum_LABELSELECTOR,
    }

}
```



