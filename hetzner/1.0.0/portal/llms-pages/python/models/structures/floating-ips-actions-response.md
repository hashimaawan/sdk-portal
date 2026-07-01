# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`List[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Required | - |


# Example

```python
from hetznercloudapi.models.action import Action
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.floating_ips_actions_response import FloatingIpsActionsResponse
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status_enum import StatusEnum

floating_ips_actions_response = FloatingIpsActionsResponse(
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
    ]
)
```



