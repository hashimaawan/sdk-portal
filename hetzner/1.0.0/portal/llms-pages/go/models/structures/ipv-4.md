# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `models.Optional[string]` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer |
| `Ip` | `models.Optional[string]` | Optional | IP address (v4) of this Load Balancer |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    ipv4 := models.Ipv4{
        DnsPtr:               models.NewOptional(models.ToPointer("lb1.example.com")),
        Ip:                   models.NewOptional(models.ToPointer("1.2.3.4")),
    }

}
```



