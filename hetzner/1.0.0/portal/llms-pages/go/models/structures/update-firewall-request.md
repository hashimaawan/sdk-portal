# Update Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`UpdateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New Firewall name |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    updateFirewallRequest := models.UpdateFirewallRequest{
        Labels:                models.ToPointer(interface{}("[labelkey, value]")),
        Name:                  models.ToPointer("new-name"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



