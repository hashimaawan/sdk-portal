# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/action.md) | Optional | - |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/image.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.action import Action
from hetznercloudapi.models.created_from import CreatedFrom
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.image import Image
from hetznercloudapi.models.os_flavor_enum import OsFlavorEnum
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.servers_actions_create_image_response import ServersActionsCreateImageResponse
from hetznercloudapi.models.status_24_enum import Status24Enum
from hetznercloudapi.models.status_enum import StatusEnum
from hetznercloudapi.models.type_22_enum import Type22Enum

servers_actions_create_image_response = ServersActionsCreateImageResponse(
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
    image=Image(
        bound_to=186,
        created='created6',
        created_from=CreatedFrom(
            id=60,
            name='name6'
        ),
        deleted='deleted4',
        deprecated='deprecated8',
        description='description6',
        disk_size=244.18,
        id=128,
        image_size=141.34,
        labels={
            'key0': 'labels4'
        },
        name='name6',
        os_flavor=OsFlavorEnum.DEBIAN,
        os_version='os_version4',
        protection=Protection(
            delete=False
        ),
        status=Status24Enum.UNAVAILABLE,
        mtype=Type22Enum.APP,
        rapid_deploy=False
    )
)
```



