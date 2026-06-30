# Ipv 44

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRklwdjQ0

IP address (v4) and its reverse DNS entry of this Server


# Class Name

`Ipv44`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Blocked` | `bool` | Required | If the IP is blocked by our anti abuse dept |
| `DnsPtr` | `string` | Required | Reverse DNS PTR entry for the IPv4 addresses of this Server |
| `Id` | `*int` | Optional | ID of the Resource |
| `Ip` | `string` | Required | IP address (v4) of this Server |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    ipv44 := models.Ipv44{
        Blocked:              false,
        DnsPtr:               "server01.example.com",
        Id:                   models.ToPointer(42),
        Ip:                   "1.2.3.4",
    }

}
```



