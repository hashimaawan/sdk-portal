# Volumes Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMg


# Class Name

`VolumesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/volume-1.md) | Required | - |


# Example

```python
from hetznercloudapi.models.location_16 import Location16
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.status_113_enum import Status113Enum
from hetznercloudapi.models.volume_1 import Volume1
from hetznercloudapi.models.volumes_response_2 import VolumesResponse2

volumes_response_2 = VolumesResponse2(
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
)
```



