# Load Balancer Target Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldFNlcnZlcg

Server where the traffic should be routed through


# Class Name

`LoadBalancerTargetServer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerTargetServer := models.LoadBalancerTargetServer{
        Id:                   80,
    }

}
```



