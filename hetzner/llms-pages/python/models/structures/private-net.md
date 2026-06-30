# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | `str` | Optional | - |
| `network` | `int` | Optional | - |


# Example

```python
from hetznercloudapi.models.private_net import PrivateNet

private_net = PrivateNet(
    ip='10.0.0.2',
    network=4711
)
```



