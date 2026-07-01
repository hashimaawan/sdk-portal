# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information


# Class Name

`PublicNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `bool` | Required | Public Interface enabled or not |
| `ipv_4` | [`Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ipv-4.md) | Required | IP address (v4) |
| `ipv_6` | [`Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ipv-6.md) | Required | IP address (v6) |


# Example

```python
from hetznercloudapi.models.ipv_4 import Ipv4
from hetznercloudapi.models.ipv_6 import Ipv6
from hetznercloudapi.models.public_net import PublicNet

public_net = PublicNet(
    enabled=False,
    ipv_4=Ipv4(
        dns_ptr='lb1.example.com',
        ip='1.2.3.4'
    ),
    ipv_6=Ipv6(
        dns_ptr='lb1.example.com',
        ip='2001:db8::1'
    )
)
```



