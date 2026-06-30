# Nullable Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRk51bGxhYmxlQWN0aW9u


# Class Name

`NullableAction`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `command` | `str` | Required | Command executed in the Action |
| `error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null |
| `finished` | `str` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. |
| `id` | `int` | Required | ID of the Resource |
| `progress` | `float` | Required | Progress of Action in percent |
| `resources` | [`List[Resource]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/resource.md) | Required | Resources the Action relates to |
| `started` | `str` | Required | Point in time when the Action was started (in ISO-8601 format) |
| `status` | [`StatusEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/status.md) | Required | Status of the Action |


# Example

```python
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.nullable_action import NullableAction
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status_enum import StatusEnum

nullable_action = NullableAction(
    command='start_server',
    error=Error(
        code='action_failed',
        message='Action failed'
    ),
    finished='2016-01-30T23:55:00+00:00',
    id=42,
    progress=100,
    resources=[
        Resource(
            id=42,
            mtype='server'
        )
    ],
    started='2016-01-30T23:55:00+00:00',
    status=StatusEnum.SUCCESS
)
```



