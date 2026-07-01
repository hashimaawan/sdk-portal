# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`


# Class Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Firewalls` | [`[]models.ServerPublicNetFirewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server |
| `FloatingIps` | `[]int` | Required | IDs of Floating IPs assigned to this Server |
| `Ipv4` | [`*models.Ipv44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server |
| `Ipv6` | [`*models.Ipv64`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    publicNet4 := models.PublicNet4{
        Firewalls:            []models.ServerPublicNetFirewall{
            models.ServerPublicNetFirewall{
                Id:                   models.ToPointer(250),
                Status:               models.ToPointer(models.Status72Enum_APPLIED),
            },
        },
        FloatingIps:          []int{
            478,
        },
        Ipv4:                 models.ToPointer(models.Ipv44{
            Blocked:              false,
            DnsPtr:               "server01.example.com",
            Id:                   models.ToPointer(42),
            Ip:                   "1.2.3.4",
        }),
        Ipv6:                 models.ToPointer(models.Ipv64{
            Blocked:              false,
            DnsPtr:               []models.DnsPtr8{
                models.DnsPtr8{
                    DnsPtr:               "server.example.com",
                    Ip:                   "2001:db8::1",
                },
            },
            Id:                   models.ToPointer(42),
            Ip:                   "2001:db8::/64",
        }),
    }

}
```



