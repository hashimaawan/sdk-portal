# Servers Actions Rebuild Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlYnVpbGQlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`ServersActionsRebuildResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Optional | - |
| `root_password` | `str` | Optional | New root password when not using SSH keys |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.action import Action
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.servers_actions_rebuild_response import ServersActionsRebuildResponse
from hetznercloudapi.models.status import Status

servers_actions_rebuild_response = ServersActionsRebuildResponse(
    action=Action(
        command='command6',
        error=Error(
            code='code2',
            message='message4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        finished='finished0',
        id=238,
        progress=143.26,
        resources=[
            Resource(
                id=198,
                mtype='type0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Resource(
                id=198,
                mtype='type0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Resource(
                id=198,
                mtype='type0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        started='started8',
        status=Status.RUNNING,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    root_password='root_password8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



