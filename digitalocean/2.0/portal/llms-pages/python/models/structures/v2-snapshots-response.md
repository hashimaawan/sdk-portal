# V2 Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2SnapshotsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshots` | [`List[Snapshot]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/snapshot.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.resource_type_1 import ResourceType1
from digitaloceanapi.models.snapshot import Snapshot
from digitaloceanapi.models.v_2_snapshots_response import V2SnapshotsResponse

v_2_snapshots_response = V2SnapshotsResponse(
    meta=Meta(
        total=1,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    snapshots=[
        Snapshot(
            id='id2',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            min_disk_size=112,
            name='name2',
            regions=[
                'regions7',
                'regions8'
            ],
            size_gigabytes=148.48,
            resource_id='resource_id8',
            resource_type=ResourceType1.DROPLET,
            tags=[
                'tags7',
                'tags8',
                'tags9'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Snapshot(
            id='id2',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            min_disk_size=112,
            name='name2',
            regions=[
                'regions7',
                'regions8'
            ],
            size_gigabytes=148.48,
            resource_id='resource_id8',
            resource_type=ResourceType1.DROPLET,
            tags=[
                'tags7',
                'tags8',
                'tags9'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Snapshot(
            id='id2',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            min_disk_size=112,
            name='name2',
            regions=[
                'regions7',
                'regions8'
            ],
            size_gigabytes=148.48,
            resource_id='resource_id8',
            resource_type=ResourceType1.DROPLET,
            tags=[
                'tags7',
                'tags8',
                'tags9'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='last6',
            next='next2',
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



