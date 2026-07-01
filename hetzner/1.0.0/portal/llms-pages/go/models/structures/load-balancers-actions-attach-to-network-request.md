# Load Balancers Actions Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQXR0YWNoJTI1MjBUbyUyNTIwTmV0d29yayUyNTIwUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`LoadBalancersActionsAttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ip` | `*string` | Optional | IP to request to be assigned to this Load Balancer; if you do not provide this then you will be auto assigned an IP address |
| `Network` | `float64` | Required | ID of an existing network to attach the Load Balancer to |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    loadBalancersActionsAttachToNetworkRequest := models.LoadBalancersActionsAttachToNetworkRequest{
        Ip:                    models.ToPointer("10.0.1.1"),
        Network:               float64(4711),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



