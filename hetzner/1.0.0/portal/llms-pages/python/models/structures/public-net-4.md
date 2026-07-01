# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`


# Class Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewalls` | [`List[ServerPublicNetFirewall]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server |
| `floating_ips` | `List[int]` | Required | IDs of Floating IPs assigned to this Server |
| `ipv_4` | [`Ipv44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server |
| `ipv_6` | [`Ipv64`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry |


# Example

```python
from hetznercloudapi.models.dns_ptr_8 import DnsPtr8
from hetznercloudapi.models.ipv_44 import Ipv44
from hetznercloudapi.models.ipv_64 import Ipv64
from hetznercloudapi.models.public_net_4 import PublicNet4
from hetznercloudapi.models.server_public_net_firewall import ServerPublicNetFirewall
from hetznercloudapi.models.status_72_enum import Status72Enum

public_net_4 = PublicNet4(
    floating_ips=[
        478
    ],
    ipv_4=Ipv44(
        blocked=False,
        dns_ptr='server01.example.com',
        ip='1.2.3.4',
        id=42
    ),
    ipv_6=Ipv64(
        blocked=False,
        dns_ptr=[
            DnsPtr8(
                dns_ptr='server.example.com',
                ip='2001:db8::1'
            )
        ],
        ip='2001:db8::/64',
        id=42
    ),
    firewalls=[
        ServerPublicNetFirewall(
            id=250,
            status=Status72Enum.APPLIED
        )
    ]
)
```



