# V2 Droplets Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwU25hcHNob3RzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DropletsSnapshotsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshots` | [`List[Backup1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/backup-1.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.backup_1 import Backup1
from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.type_13 import Type13
from digitaloceanapi.models.v_2_droplets_snapshots_response import V2DropletsSnapshotsResponse

v_2_droplets_snapshots_response = V2DropletsSnapshotsResponse(
    meta=Meta(
        total=1,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    snapshots=[
        Backup1(
            id=66,
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            min_disk_size=112,
            name='name2',
            regions=[
                'regions7',
                'regions8'
            ],
            size_gigabytes=148.48,
            mtype=Type13.SNAPSHOT,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Backup1(
            id=66,
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            min_disk_size=112,
            name='name2',
            regions=[
                'regions7',
                'regions8'
            ],
            size_gigabytes=148.48,
            mtype=Type13.SNAPSHOT,
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



