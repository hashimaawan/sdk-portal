# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer


# Class Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`models.Type28Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-28.md) | Required | Type of the algorithm |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerAlgorithm := models.LoadBalancerAlgorithm{
        Type:                 models.Type28Enum_ROUNDROBIN,
    }

}
```



