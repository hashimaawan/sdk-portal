# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AliasIps` | `[]string` | Required | New alias IPs to set for this Server |
| `Network` | `int` | Required | ID of an existing Network already attached to the Server |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsChangeAliasIpsRequest := models.ServersActionsChangeAliasIpsRequest{
        AliasIps:             []string{
            "10.0.1.2",
        },
        Network:              4711,
    }

}
```



