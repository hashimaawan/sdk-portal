# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type interface{}.*


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ListenPort` | `float64` | Required | The listen port of the service you want to delete |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    loadBalancersActionsDeleteServiceRequest := models.LoadBalancersActionsDeleteServiceRequest{
        ListenPort:            float64(4711),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



