# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q


# Class Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`models.Type39Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancersActionsChangeAlgorithmRequest := models.LoadBalancersActionsChangeAlgorithmRequest{
        Type:                 models.Type39Enum_ROUNDROBIN,
    }

}
```



