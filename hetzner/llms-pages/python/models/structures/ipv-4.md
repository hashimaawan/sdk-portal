# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `str` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer |
| `ip` | `str` | Optional | IP address (v4) of this Load Balancer |


# Example

```python
from hetznercloudapi.models.ipv_4 import Ipv4

ipv_4 = Ipv4(
    dns_ptr='lb1.example.com',
    ip='1.2.3.4'
)
```



