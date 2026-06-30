# Public Net 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlB1YmxpY05ldDU

Public Network options


# Class Name

`PublicNet5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EnableIpv4` | `*bool` | Optional | Attach an IPv4 on the public NIC. If false, no IPv4 address will be attached. Defaults to true. |
| `EnableIpv6` | `*bool` | Optional | Attach an IPv6 on the public NIC. If false, no IPv6 address will be attached. Defaults to true. |
| `Ipv4` | `models.Optional[int]` | Optional | ID of the ipv4 Primary IP to use. If omitted and enable_ipv4 is true, a new ipv4 Primary IP will automatically be created. |
| `Ipv6` | `models.Optional[int]` | Optional | ID of the ipv6 Primary IP to use. If omitted and enable_ipv6 is true, a new ipv6 Primary IP will automatically be created. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    publicNet5 := models.PublicNet5{
        EnableIpv4:           models.ToPointer(false),
        EnableIpv6:           models.ToPointer(false),
        Ipv4:                 models.NewOptional(models.ToPointer(42)),
        Ipv6:                 models.NewOptional(models.ToPointer(102)),
    }

}
```



