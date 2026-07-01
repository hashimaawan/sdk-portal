# Ipv 64

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRklwdjY0

IPv6 network assigned to this Server and its reverse DNS entry


# Class Name

`Ipv64`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `bool` | Required | If the IP is blocked by our anti abuse dept |
| `dns_ptr` | [`List[DnsPtr8]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/dns-ptr-8.md) | Required | Reverse DNS PTR entries for the IPv6 addresses of this Server, `null` by default |
| `id` | `int` | Optional | ID of the Resource |
| `ip` | `str` | Required | IP address (v6) of this Server |


# Example

```python
from hetznercloudapi.models.dns_ptr_8 import DnsPtr8
from hetznercloudapi.models.ipv_64 import Ipv64

ipv_64 = Ipv64(
    blocked=False,
    dns_ptr=[
        DnsPtr8(
            dns_ptr='server.example.com',
            ip='2001:db8::1'
        )
    ],
    ip='2001:db8::/64',
    id=42
)
```



