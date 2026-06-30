# Create Load Balancer Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUxvYWRCYWxhbmNlclJlcXVlc3Q


# Class Name

`CreateLoadBalancerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Algorithm` | [`models.LoadBalancerAlgorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/load-balancer-algorithm.md) | Required | Algorithm of the Load Balancer |
| `Labels` | [`*models.Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `LoadBalancerType` | `string` | Required | ID or name of the Load Balancer type this Load Balancer should be created with |
| `Location` | `*string` | Optional | ID or name of Location to create Load Balancer in |
| `Name` | `string` | Required | Name of the Load Balancer |
| `Network` | `*int` | Optional | ID of the network the Load Balancer should be attached to on creation |
| `NetworkZone` | `*string` | Optional | Name of network zone |
| `PublicInterface` | `*bool` | Optional | Enable or disable the public interface of the Load Balancer |
| `Services` | [`[]models.LoadBalancerService`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/load-balancer-service.md) | Optional | Array of services |
| `Targets` | [`[]models.LoadBalancerTarget`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/load-balancer-target.md) | Optional | Array of targets |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createLoadBalancerRequest := models.CreateLoadBalancerRequest{
        Algorithm:            models.LoadBalancerAlgorithm{
            Type:                 models.Type28Enum_ROUNDROBIN,
        },
        Labels:               models.ToPointer(models.Labels{
            Labelkey:             models.ToPointer("labelkey4"),
        }),
        LoadBalancerType:     "lb11",
        Location:             models.ToPointer("location2"),
        Name:                 "Web Frontend",
        Network:              models.ToPointer(123),
        NetworkZone:          models.ToPointer("eu-central"),
        PublicInterface:      models.ToPointer(true),
    }

}
```



