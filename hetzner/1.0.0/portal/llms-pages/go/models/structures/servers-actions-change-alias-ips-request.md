# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AliasIps` | `[]string` | Required | New alias IPs to set for this Server |
| `Network` | `int` | Required | ID of an existing Network already attached to the Server |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serversActionsChangeAliasIpsRequest := models.ServersActionsChangeAliasIpsRequest{
        AliasIps:              []string{
            "10.0.1.2",
        },
        Network:               4711,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



