# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type Any.*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bound_to` | `int` | Required | ID of Server the Image is bound to. Only set for Images of type `backup`. |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `created_from` | [`CreatedFrom`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/created-from.md) | Required | Information about the Server the Image was created from |
| `deleted` | `str` | Required | Point in time where the Image was deleted (in ISO-8601 format) |
| `deprecated` | `str` | Required | Point in time when the Image is considered to be deprecated (in ISO-8601 format) |
| `description` | `str` | Required | Description of the Image |
| `disk_size` | `float` | Required | Size of the disk contained in the Image in GB |
| `id` | `int` | Required | ID of the Resource |
| `image_size` | `float` | Required | Size of the Image file in our storage in GB. For snapshot Images this is the value relevant for calculating costs for the Image. |
| `labels` | `Dict[str, str]` | Required | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Unique identifier of the Image. This value is only set for system Images. |
| `os_flavor` | [`OsFlavor`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/os-flavor.md) | Required | Flavor of operating system contained in the Image |
| `os_version` | `str` | Required | Operating system version |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `rapid_deploy` | `bool` | Optional | Indicates that rapid deploy of the Image is available |
| `status` | [`Status24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/status-24.md) | Required | Whether the Image can be used or if it's still being created or unavailable |
| `mtype` | [`Type22`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-22.md) | Required | Type of the Image |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.created_from import CreatedFrom
from hetznercloudapi.models.image import Image
from hetznercloudapi.models.os_flavor import OsFlavor
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.status_24 import Status24
from hetznercloudapi.models.type_22 import Type22

image = Image(
    bound_to=None,
    created='2016-01-30T23:55:00+00:00',
    created_from=CreatedFrom(
        id=1,
        name='Server',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    deleted=None,
    deprecated='2018-02-28T00:00:00+00:00',
    description='Ubuntu 20.04 Standard 64 bit',
    disk_size=10,
    id=42,
    image_size=2.3,
    labels={
        'key0': 'labels4'
    },
    name='ubuntu-20.04',
    os_flavor=OsFlavor.UBUNTU,
    os_version='20.04',
    protection=Protection(
        delete=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    status=Status24.UNAVAILABLE,
    mtype=Type22.SNAPSHOT,
    rapid_deploy=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



