# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkRuc1B0cg


# Class Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Required | DNS pointer for the specific IP address |
| `Ip` | `string` | Required | Single IPv4 or IPv6 address |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    dnsPtr := models.DnsPtr{
        DnsPtr:               "server.example.com",
        Ip:                   "2001:db8::1",
    }

}
```



