# Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Any.*


# Class Name

`VolumesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Required | - |
| `next_actions` | [`List[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Required | - |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/volume-1.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.action import Action
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.location_16 import Location16
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status import Status
from hetznercloudapi.models.status_113 import Status113
from hetznercloudapi.models.volume_1 import Volume1
from hetznercloudapi.models.volumes_response_1 import VolumesResponse1

volumes_response_1 = VolumesResponse1(
    action=Action(
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
        status=Status.RUNNING,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    next_actions=[
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
    volume=Volume1(
        created='2016-01-30T23:55:00+00:00',
        format='xfs',
        id=42,
        labels={
            'key0': 'labels8',
            'key1': 'labels9',
            'key2': 'labels0'
        },
        linux_device='/dev/disk/by-id/scsi-0HC_Volume_4711',
        location=Location16(
            city='Falkenstein',
            country='DE',
            description='Falkenstein DC Park 1',
            id=1,
            latitude=50.47612,
            longitude=12.370071,
            name='fsn1',
            network_zone='eu-central',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        name='my-resource',
        protection=Protection(
            delete=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        server=12,
        size=42,
        status=Status113.AVAILABLE,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



