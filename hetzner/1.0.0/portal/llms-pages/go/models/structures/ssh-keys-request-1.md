# Ssh Keys Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdDE

*This model accepts additional fields of type interface{}.*


# Class Name

`SshKeysRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New name Name to set |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    sshKeysRequest1 := models.SshKeysRequest1{
        Labels:                models.ToPointer(interface{}("[labelkey, value]")),
        Name:                  models.ToPointer("My ssh key"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



