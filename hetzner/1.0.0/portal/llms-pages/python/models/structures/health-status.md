# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw

*This model accepts additional fields of type Any.*


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listen_port` | `int` | Optional | - |
| `status` | [`Status30`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/status-30.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.health_status import HealthStatus
from hetznercloudapi.models.status_30 import Status30

health_status = HealthStatus(
    listen_port=443,
    status=Status30.HEALTHY,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



