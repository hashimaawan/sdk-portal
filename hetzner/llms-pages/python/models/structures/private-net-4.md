# Private Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ0


# Class Name

`PrivateNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `List[str]` | Optional | - |
| `ip` | `str` | Optional | - |
| `mac_address` | `str` | Optional | - |
| `network` | `int` | Optional | - |


# Example

```python
from hetznercloudapi.models.private_net_4 import PrivateNet4

private_net_4 = PrivateNet4(
    alias_ips=[
        'alias_ips0'
    ],
    ip='10.0.0.2',
    mac_address='86:00:ff:2a:7d:e1',
    network=4711
)
```



