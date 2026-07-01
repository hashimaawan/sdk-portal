# Nullable Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRk51bGxhYmxlQWN0aW9u

*This model accepts additional fields of type Any.*


# Class Name

`NullableAction`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `command` | `str` | Required | Command executed in the Action |
| `error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null |
| `finished` | `str` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. |
| `id` | `int` | Required | ID of the Resource |
| `progress` | `float` | Required | Progress of Action in percent |
| `resources` | [`List[Resource]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/resource.md) | Required | Resources the Action relates to |
| `started` | `str` | Required | Point in time when the Action was started (in ISO-8601 format) |
| `status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/status.md) | Required | Status of the Action |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.error import Error
from hetznercloudapi.models.nullable_action import NullableAction
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status import Status

nullable_action = NullableAction(
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
```



