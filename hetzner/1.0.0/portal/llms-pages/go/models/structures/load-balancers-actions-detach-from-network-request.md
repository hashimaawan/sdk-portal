# Load Balancers Actions Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGV0YWNoJTI1MjBGcm9tJTI1MjBOZXR3b3JrJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type interface{}.*


# Class Name

`LoadBalancersActionsDetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Network` | `float64` | Required | ID of an existing network to detach the Load Balancer from |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    loadBalancersActionsDetachFromNetworkRequest := models.LoadBalancersActionsDetachFromNetworkRequest{
        Network:               float64(4711),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



