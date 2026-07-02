# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `str` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. |
| `description` | `str` | Optional | An optional free-form text field to describe a block storage volume. |
| `droplet_ids` | `List[int]` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. |
| `id` | `str` | Optional, Read-only | The unique identifier for the block storage volume. |
| `name` | `str` | Optional | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. |
| `size_gigabytes` | `int` | Optional | The size of the block storage volume in GiB (1024^3). |
| `tags` | `List[str]` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `filesystem_label` | `str` | Optional | The label currently applied to the filesystem. |
| `filesystem_type` | `str` | Optional | The type of filesystem currently in-use on the volume. |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/region.md) | Optional, Read-only | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.region import Region
from digitaloceanapi.models.volume import Volume

volume = Volume(
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
```



