# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`List[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.action import Action
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.floating_ips_actions_response import FloatingIpsActionsResponse
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status import Status

floating_ips_actions_response = FloatingIpsActionsResponse(
    actions=[
        Action(
            command='start_server',
            error=Error(
                code='action_failed',
                message='Action failed',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            finished='2016-01-30T23:55:00+00:00',
            id=42,
            progress=100,
            resources=[
                Resource(
                    id=42,
                    mtype='server',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            started='2016-01-30T23:55:00+00:00',
            status=Status.SUCCESS,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



