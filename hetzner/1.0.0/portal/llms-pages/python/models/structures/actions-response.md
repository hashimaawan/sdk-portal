# Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFjdGlvbnNSZXNwb25zZQ


# Class Name

`ActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`List[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/meta.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.action import Action
from hetznercloudapi.models.actions_response import ActionsResponse
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status_enum import StatusEnum

actions_response = ActionsResponse(
    actions=[
        Action(
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
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64
        )
    )
)
```



