# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkRuc1B0cjg


# Class Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Required | DNS pointer for the specific IP address |
| `Ip` | `string` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    dnsPtr8 := models.DnsPtr8{
        DnsPtr:               "server.example.com",
        Ip:                   "2001:db8::1",
    }

}
```



