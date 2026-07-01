# Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`VolumesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/meta.md) | Optional | - |
| `volumes` | [`List[Volume1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/volume-1.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.location_16 import Location16
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.status_113 import Status113
from hetznercloudapi.models.volume_1 import Volume1
from hetznercloudapi.models.volumes_response import VolumesResponse

volumes_response = VolumesResponse(
    volumes=[
        Volume1(
            created='2016-01-30T23:55:00+00:00',
            format='xfs',
            id=42,
            labels={
                'key0': 'labels4'
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
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



