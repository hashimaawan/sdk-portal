# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `*int` | Optional | ID of the Resource |
| `Status` | [`*models.Status72Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serverPublicNetFirewall := models.ServerPublicNetFirewall{
        Id:                   models.ToPointer(42),
        Status:               models.ToPointer(models.Status72Enum_APPLIED),
    }

}
```



