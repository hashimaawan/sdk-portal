# Private Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ0

*This model accepts additional fields of type interface{}.*


# Class Name

`PrivateNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AliasIps` | `[]string` | Optional | - |
| `Ip` | `*string` | Optional | - |
| `MacAddress` | `*string` | Optional | - |
| `Network` | `*int` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    privateNet4 := models.PrivateNet4{
        AliasIps:              []string{
            "alias_ips0",
            "alias_ips9",
        },
        Ip:                    models.ToPointer("10.0.0.2"),
        MacAddress:            models.ToPointer("86:00:ff:2a:7d:e1"),
        Network:               models.ToPointer(4711),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



