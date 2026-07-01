# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0

*This model accepts additional fields of type interface{}.*


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancerType` | `string` | Required | ID or name of Load Balancer type the Load Balancer should migrate to |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    changeTypeRequest := models.ChangeTypeRequest{
        LoadBalancerType:      "lb21",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



