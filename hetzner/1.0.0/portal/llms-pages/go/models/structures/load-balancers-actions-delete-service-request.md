# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ListenPort` | `float64` | Required | The listen port of the service you want to delete |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancersActionsDeleteServiceRequest := models.LoadBalancersActionsDeleteServiceRequest{
        ListenPort:           float64(4711),
    }

}
```



