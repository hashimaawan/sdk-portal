# V2 Volumes Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2VolumesSnapshotsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshot` | [`Snapshot`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/snapshot.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.resource_type_1 import ResourceType1
from digitaloceanapi.models.snapshot import Snapshot
from digitaloceanapi.models.v_2_volumes_snapshots_response import V2VolumesSnapshotsResponse

v_2_volumes_snapshots_response = V2VolumesSnapshotsResponse(
    snapshot=Snapshot(
        id='8fa70202-873f-11e6-8b68-000f533176b1',
        created_at=dateutil.parser.parse('2020-09-30T18:56:14Z'),
        min_disk_size=10,
        name='big-data-snapshot1475261774',
        regions=[
            'nyc1'
        ],
        size_gigabytes=10,
        resource_id='82a48a18-873f-11e6-96bf-000f53315a41',
        resource_type=ResourceType1.VOLUME,
        tags=[
            'aninterestingtag'
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



