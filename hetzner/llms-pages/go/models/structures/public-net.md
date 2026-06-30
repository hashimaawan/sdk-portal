# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information


# Class Name

`PublicNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `bool` | Required | Public Interface enabled or not |
| `Ipv4` | [`models.Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/ipv-4.md) | Required | IP address (v4) |
| `Ipv6` | [`models.Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/ipv-6.md) | Required | IP address (v6) |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    publicNet := models.PublicNet{
        Enabled:              false,
        Ipv4:                 models.Ipv4{
            DnsPtr:               models.NewOptional(models.ToPointer("lb1.example.com")),
            Ip:                   models.NewOptional(models.ToPointer("1.2.3.4")),
        },
        Ipv6:                 models.Ipv6{
            DnsPtr:               models.NewOptional(models.ToPointer("lb1.example.com")),
            Ip:                   models.NewOptional(models.ToPointer("2001:db8::1")),
        },
    }

}
```



