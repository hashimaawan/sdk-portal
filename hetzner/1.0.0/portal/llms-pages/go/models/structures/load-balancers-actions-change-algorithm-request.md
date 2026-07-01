# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`models.Type39`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    loadBalancersActionsChangeAlgorithmRequest := models.LoadBalancersActionsChangeAlgorithmRequest{
        Type:                  models.Type39_RoundRobin,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



