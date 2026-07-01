# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`UpdatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutoDelete` | `*bool` | Optional | Delete this Primary IP when the resource it is assigned to is deleted |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New unique name to set |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    updatePrimaryIpRequest := models.UpdatePrimaryIpRequest{
        AutoDelete:            models.ToPointer(true),
        Labels:                models.ToPointer(interface{}("[labelkey, value]")),
        Name:                  models.ToPointer("my-ip"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



