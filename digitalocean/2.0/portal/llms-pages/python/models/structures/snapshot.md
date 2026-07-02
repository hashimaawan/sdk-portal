# Snapshot

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlNuYXBzaG90

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Snapshot`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Required | The unique identifier for the snapshot. |
| `created_at` | `datetime` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. |
| `min_disk_size` | `int` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. |
| `name` | `str` | Required | A human-readable name for the snapshot. |
| `regions` | `List[str]` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. |
| `size_gigabytes` | `float` | Required | The billable size of the snapshot in gigabytes. |
| `resource_id` | `str` | Required | The unique identifier for the resource that the snapshot originated from. |
| `resource_type` | [`ResourceType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/resource-type-1.md) | Required | The type of resource that the snapshot originated from. |
| `tags` | `List[str]` | Required | An array of Tags the snapshot has been tagged with. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.resource_type_1 import ResourceType1
from digitaloceanapi.models.snapshot import Snapshot

snapshot = Snapshot(
    id='6372321',
    created_at=dateutil.parser.parse('2020-07-28T16:47:44Z'),
    min_disk_size=25,
    name='web-01-1595954862243',
    regions=[
        'nyc3',
        'sfo3'
    ],
    size_gigabytes=2.34,
    resource_id='200776916',
    resource_type=ResourceType1.DROPLET,
    tags=[
        'web',
        'env:prod'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



