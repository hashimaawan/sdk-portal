# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listen_port` | `int` | Optional | - |
| `status` | [`Status30Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/status-30.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.health_status import HealthStatus
from hetznercloudapi.models.status_30_enum import Status30Enum

health_status = HealthStatus(
    listen_port=443,
    status=Status30Enum.HEALTHY
)
```



