# Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFsZ29yaXRobQ

Algorithm of the Load Balancer

*This model accepts additional fields of type interface{}.*


# Class Name

`Algorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`models.Type28`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-28.md) | Required | Type of the algorithm |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    algorithm := models.Algorithm{
        Type:                  models.Type28_RoundRobin,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



