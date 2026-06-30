# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlRhcmdldA


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `health_status` | [`List[HealthStatus]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/health-status.md) | Optional | - |
| `server` | [`Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/server-11.md) | Optional | - |
| `mtype` | `str` | Optional | - |
| `use_private_ip` | `bool` | Optional | - |


# Example

```python
from hetznercloudapi.models.health_status import HealthStatus
from hetznercloudapi.models.server_11 import Server11
from hetznercloudapi.models.status_30_enum import Status30Enum
from hetznercloudapi.models.target import Target

target = Target(
    health_status=[
        HealthStatus(
            listen_port=142,
            status=Status30Enum.UNKNOWN
        ),
        HealthStatus(
            listen_port=142,
            status=Status30Enum.UNKNOWN
        ),
        HealthStatus(
            listen_port=142,
            status=Status30Enum.UNKNOWN
        )
    ],
    server=Server11(
        id=14
    ),
    mtype='server',
    use_private_ip=False
)
```



