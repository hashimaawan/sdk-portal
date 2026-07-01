# Add Target Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFkZFRhcmdldFJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`AddTargetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ip` | [`*models.Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `LabelSelector` | [`*models.LabelSelector12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/label-selector-12.md) | Optional | Configuration for label selector targets, required if type is `label_selector` |
| `Server` | [`*models.Server16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-16.md) | Optional | Configuration for type Server, required if type is `server` |
| `Type` | [`models.Type29`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-29.md) | Required | Type of the resource |
| `UsePrivateIp` | `*bool` | Optional | Use the private network IP instead of the public IP of the Server, requires the Server and Load Balancer to be in the same network. Default value is false. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    addTargetRequest := models.AddTargetRequest{
        Ip:                    models.ToPointer(models.Ip{
            Ip:                    "ip8",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        LabelSelector:         models.ToPointer(models.LabelSelector12{
            Selector:              "selector8",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Server:                models.ToPointer(models.Server16{
            Id: float64(217.74),
        }),
        Type:                  models.Type29_Server,
        UsePrivateIp:          models.ToPointer(true),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



