# Firewall 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkZpcmV3YWxsNA

*This model accepts additional fields of type interface{}.*


# Class Name

`Firewall4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Firewall` | `*int` | Optional | ID of the Firewall |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    firewall4 := models.Firewall4{
        Firewall:              models.ToPointer(176),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



