# V2 Snapshots Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2SnapshotsResponse1`


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
from digitaloceanapi.models.v_2_snapshots_response_1 import V2SnapshotsResponse1

v_2_snapshots_response_1 = V2SnapshotsResponse1(
    snapshot=Snapshot(
        id='id8',
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        min_disk_size=36,
        name='name8',
        regions=[
            'regions3',
            'regions4',
            'regions5'
        ],
        size_gigabytes=140.04,
        resource_id='resource_id4',
        resource_type=ResourceType1.DROPLET,
        tags=[
            'tags3'
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



