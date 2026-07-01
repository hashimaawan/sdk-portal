# Action Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFjdGlvblJlc3BvbnNl


# Class Name

`ActionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Required | - |


# Example

```python
from hetznercloudapi.models.action import Action
from hetznercloudapi.models.action_response import ActionResponse
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status_enum import StatusEnum

action_response = ActionResponse(
    action=Action(
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
        status=StatusEnum.RUNNING
    )
)
```



