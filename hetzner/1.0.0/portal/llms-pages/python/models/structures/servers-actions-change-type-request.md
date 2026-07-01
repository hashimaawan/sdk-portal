# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server_type` | `str` | Required | ID or name of Server type the Server should migrate to |
| `upgrade_disk` | `bool` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.servers_actions_change_type_request import ServersActionsChangeTypeRequest

servers_actions_change_type_request = ServersActionsChangeTypeRequest(
    server_type='cx11',
    upgrade_disk=True,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



