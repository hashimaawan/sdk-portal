# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ssh_keys` | `List[int]` | Optional | Array of SSH key IDs which should be injected into the rescue system. |
| `mtype` | [`Type65`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.servers_actions_enable_rescue_request import ServersActionsEnableRescueRequest
from hetznercloudapi.models.type_65 import Type65

servers_actions_enable_rescue_request = ServersActionsEnableRescueRequest(
    ssh_keys=[
        2323
    ],
    mtype=Type65.LINUX64,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



