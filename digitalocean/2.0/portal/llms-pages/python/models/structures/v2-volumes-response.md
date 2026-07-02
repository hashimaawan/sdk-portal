# V2 Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2VolumesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `volumes` | [`List[Volume]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/volume.md) | Required | Array of volumes. |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.v_2_volumes_response import V2VolumesResponse
from digitaloceanapi.models.volume import Volume

v_2_volumes_response = V2VolumesResponse(
    volumes=[
        Volume(
            created_at='2020-03-02T17:00:49Z',
            description='Block store for examples',
            droplet_ids=[],
            id='506f78a4-e098-11e5-ad9f-000f53306ae1',
            name='example',
            size_gigabytes=10,
            tags=[
                'base-image',
                'prod'
            ],
            filesystem_label='example',
            filesystem_type='ext4',
            region=Region(
                available=True,
                features=[
                    'private_networking',
                    'backups',
                    'ipv6',
                    'metadata'
                ],
                name='New York 1',
                sizes=[
                    's-1vcpu-1gb',
                    's-1vcpu-2gb',
                    's-1vcpu-3gb',
                    's-2vcpu-2gb',
                    's-3vcpu-1gb',
                    's-2vcpu-4gb',
                    's-4vcpu-8gb',
                    's-6vcpu-16gb',
                    's-8vcpu-32gb',
                    's-12vcpu-48gb',
                    's-16vcpu-64gb',
                    's-20vcpu-96gb',
                    's-24vcpu-128gb',
                    's-32vcpu-192gb'
                ],
                slug='nyc1'
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    meta=Meta(
        total=1,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
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



