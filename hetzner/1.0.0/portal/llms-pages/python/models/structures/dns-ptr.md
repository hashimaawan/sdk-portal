# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkRuc1B0cg


# Class Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `str` | Required | DNS pointer for the specific IP address |
| `ip` | `str` | Required | Single IPv4 or IPv6 address |


# Example

```python
from hetznercloudapi.models.dns_ptr import DnsPtr

dns_ptr = DnsPtr(
    dns_ptr='server.example.com',
    ip='2001:db8::1'
)
```



