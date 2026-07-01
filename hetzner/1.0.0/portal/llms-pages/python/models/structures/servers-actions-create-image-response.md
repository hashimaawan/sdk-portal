# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Optional | - |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.action import Action
from hetznercloudapi.models.created_from import CreatedFrom
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.image import Image
from hetznercloudapi.models.os_flavor import OsFlavor
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.servers_actions_create_image_response import ServersActionsCreateImageResponse
from hetznercloudapi.models.status import Status
from hetznercloudapi.models.status_24 import Status24
from hetznercloudapi.models.type_22 import Type22

servers_actions_create_image_response = ServersActionsCreateImageResponse(
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
    image=Image(
        bound_to=186,
        created='created6',
        created_from=CreatedFrom(
            id=60,
            name='name6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
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
        os_flavor=OsFlavor.DEBIAN,
        os_version='os_version4',
        protection=Protection(
            delete=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        status=Status24.UNAVAILABLE,
        mtype=Type22.APP,
        rapid_deploy=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



