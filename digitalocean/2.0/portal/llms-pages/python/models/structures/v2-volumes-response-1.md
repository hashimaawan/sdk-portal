# V2 Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2VolumesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/volume.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.region import Region
from digitaloceanapi.models.v_2_volumes_response_1 import V2VolumesResponse1
from digitaloceanapi.models.volume import Volume

v_2_volumes_response_1 = V2VolumesResponse1(
    volume=Volume(
        created_at='2020-03-02T17:00:49Z',
        description='Block store for examples',
        droplet_ids=[],
        id='506f78a4-e098-11e5-ad9f-000f53306ae1',
        name='example',
        size_gigabytes=10,
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
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



