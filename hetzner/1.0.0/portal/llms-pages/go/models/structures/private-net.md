# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ip` | `*string` | Optional | - |
| `Network` | `*int` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    privateNet := models.PrivateNet{
        Ip:                    models.ToPointer("10.0.0.2"),
        Network:               models.ToPointer(4711),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



