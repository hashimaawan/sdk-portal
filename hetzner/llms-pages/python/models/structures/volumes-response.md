# Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNl


# Class Name

`VolumesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/meta.md) | Optional | - |
| `volumes` | [`List[Volume1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/volume-1.md) | Required | - |


# Example

```python
from hetznercloudapi.models.location_16 import Location16
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.status_113_enum import Status113Enum
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
                network_zone='eu-central'
            ),
            name='my-resource',
            protection=Protection(
                delete=False
            ),
            server=12,
            size=42,
            status=Status113Enum.AVAILABLE
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



