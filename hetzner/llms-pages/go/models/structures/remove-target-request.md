# Remove Target Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlJlbW92ZVRhcmdldFJlcXVlc3Q


# Class Name

`RemoveTargetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ip` | [`*models.Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `LabelSelector` | [`*models.LabelSelector12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/label-selector-12.md) | Optional | Configuration for label selector targets, required if type is `label_selector` |
| `Server` | [`*models.Server16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/server-16.md) | Optional | Configuration for type Server, required if type is `server` |
| `Type` | [`models.Type29Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-29.md) | Required | Type of the resource |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    removeTargetRequest := models.RemoveTargetRequest{
        Ip:                   models.ToPointer(models.Ip{
            Ip:                   "ip8",
        }),
        LabelSelector:        models.ToPointer(models.LabelSelector12{
            Selector:             "selector8",
        }),
        Server:               models.ToPointer(models.Server16{
            Id: float64(217.74),
        }),
        Type:                 models.Type29Enum_IP,
    }

}
```



