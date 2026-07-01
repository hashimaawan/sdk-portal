# Load Balancers Actions Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGV0YWNoJTI1MjBGcm9tJTI1MjBOZXR3b3JrJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Network` | `float64` | Required | ID of an existing network to detach the Load Balancer from |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancersActionsDetachFromNetworkRequest := models.LoadBalancersActionsDetachFromNetworkRequest{
        Network:              float64(4711),
    }

}
```



