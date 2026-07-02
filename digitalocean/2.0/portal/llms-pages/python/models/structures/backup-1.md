# Backup 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkJhY2t1cDE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Backup1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Required | The unique identifier for the snapshot or backup. |
| `created_at` | `datetime` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. |
| `min_disk_size` | `int` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. |
| `name` | `str` | Required | A human-readable name for the snapshot. |
| `regions` | `List[str]` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. |
| `size_gigabytes` | `float` | Required | The billable size of the snapshot in gigabytes. |
| `mtype` | [`Type13`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-13.md) | Required | Describes the kind of image. It may be one of `snapshot` or `backup`. This specifies whether an image is a user-generated Droplet snapshot or automatically created Droplet backup. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.backup_1 import Backup1
from digitaloceanapi.models.type_13 import Type13

backup_1 = Backup1(
    id=6372321,
    created_at=dateutil.parser.parse('2020-07-28T16:47:44Z'),
    min_disk_size=25,
    name='web-01-1595954862243',
    regions=[
        'nyc3',
        'sfo3'
    ],
    size_gigabytes=2.34,
    mtype=Type13.SNAPSHOT,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



