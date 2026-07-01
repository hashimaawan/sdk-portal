# Load Balancers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVxdWVzdA


# Class Name

`LoadBalancersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New Load Balancer name |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancersRequest := models.LoadBalancersRequest{
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Name:                 models.ToPointer("new-name"),
    }

}
```



