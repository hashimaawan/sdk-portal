# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRklwdjY

IP address (v6)


# Class Name

`Ipv6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `str` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer |
| `ip` | `str` | Optional | IP address (v6) of this Load Balancer |


# Example

```python
from hetznercloudapi.models.ipv_6 import Ipv6

ipv_6 = Ipv6(
    dns_ptr='lb1.example.com',
    ip='2001:db8::1'
)
```



