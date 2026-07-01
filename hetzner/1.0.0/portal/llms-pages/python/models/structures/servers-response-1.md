# Servers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMQ


# Class Name

`ServersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.action import Action
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.servers_response_1 import ServersResponse1
from hetznercloudapi.models.status_enum import StatusEnum

servers_response_1 = ServersResponse1(
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
    )
)
```



