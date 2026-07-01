# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlRhcmdldA

*This model accepts additional fields of type Any.*


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `health_status` | [`List[HealthStatus]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/health-status.md) | Optional | - |
| `server` | [`Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-11.md) | Optional | - |
| `mtype` | `str` | Optional | - |
| `use_private_ip` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.health_status import HealthStatus
from hetznercloudapi.models.server_11 import Server11
from hetznercloudapi.models.status_30 import Status30
from hetznercloudapi.models.target import Target

target = Target(
    health_status=[
        HealthStatus(
            listen_port=142,
            status=Status30.UNKNOWN,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        HealthStatus(
            listen_port=142,
            status=Status30.UNKNOWN,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        HealthStatus(
            listen_port=142,
            status=Status30.UNKNOWN,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    server=Server11(
        id=14,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    mtype='server',
    use_private_ip=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



