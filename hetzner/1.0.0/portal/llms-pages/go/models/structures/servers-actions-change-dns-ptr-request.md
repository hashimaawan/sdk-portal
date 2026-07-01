# Servers Actions Change Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwRG5zJTI1MjBQdHIlMjUyMFJlcXVlc3Q


# Class Name

`ServersActionsChangeDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `*string` | Required | Hostname to set as a reverse DNS PTR entry, reset to original value if `null` |
| `Ip` | `string` | Required | Primary IP address for which the reverse DNS entry should be set |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsChangeDnsPtrRequest := models.ServersActionsChangeDnsPtrRequest{
        DnsPtr:               models.ToPointer("server01.example.com"),
        Ip:                   "1.2.3.4",
    }

}
```



