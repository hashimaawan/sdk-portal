# Volume 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZTE

*This model accepts additional fields of type Any.*


# Class Name

`Volume1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `format` | `str` | Required | Filesystem of the Volume if formatted on creation, null if not formatted on creation |
| `id` | `int` | Required | ID of the Resource |
| `labels` | `Dict[str, str]` | Required | User-defined labels (key-value pairs) |
| `linux_device` | `str` | Required | Device path on the file system for the Volume |
| `location` | [`Location16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/location-16.md) | Required | Location of the Volume. Volume can only be attached to Servers in the same Location. |
| `name` | `str` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `server` | `int` | Required | ID of the Server the Volume is attached to, null if it is not attached at all |
| `size` | `float` | Required | Size in GB of the Volume |
| `status` | [`Status113`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/status-113.md) | Required | Current status of the Volume |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.location_16 import Location16
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.status_113 import Status113
from hetznercloudapi.models.volume_1 import Volume1

volume_1 = Volume1(
    created='2016-01-30T23:55:00+00:00',
    format='xfs',
    id=42,
    labels={
        'key0': 'labels6',
        'key1': 'labels7'
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
        network_zone='eu-central',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    name='my-resource',
    protection=Protection(
        delete=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    server=12,
    size=42,
    status=Status113.AVAILABLE,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



