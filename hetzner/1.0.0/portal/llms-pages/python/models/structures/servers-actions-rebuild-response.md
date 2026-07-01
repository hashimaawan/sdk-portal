# Servers Actions Rebuild Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlYnVpbGQlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsRebuildResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Optional | - |
| `root_password` | `str` | Optional | New root password when not using SSH keys |


# Example

```python
from hetznercloudapi.models.action import Action
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.servers_actions_rebuild_response import ServersActionsRebuildResponse
from hetznercloudapi.models.status_enum import StatusEnum

servers_actions_rebuild_response = ServersActionsRebuildResponse(
    action=Action(
        command='command6',
        error=Error(
            code='code2',
            message='message4'
        ),
        finished='finished0',
        id=238,
        progress=143.26,
        resources=[
            Resource(
                id=198,
                mtype='type0'
            ),
            Resource(
                id=198,
                mtype='type0'
            ),
            Resource(
                id=198,
                mtype='type0'
            )
        ],
        started='started8',
        status=StatusEnum.RUNNING
    ),
    root_password='root_password8'
)
```



