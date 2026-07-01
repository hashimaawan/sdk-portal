# Datacenter

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFjZW50ZXI

*This model accepts additional fields of type Any.*


# Class Name

`Datacenter`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Required | Description of the Datacenter |
| `id` | `int` | Required | ID of the Resource |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/location.md) | Required | - |
| `name` | `str` | Required | Unique identifier of the Datacenter |
| `server_types` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-types.md) | Required | The Server types the Datacenter can handle |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.datacenter import Datacenter
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.server_types import ServerTypes

datacenter = Datacenter(
    description='Falkenstein DC Park 8',
    id=42,
    location=Location(
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
    name='fsn1-dc8',
    server_types=ServerTypes(
        available=[
            1,
            2,
            3
        ],
        available_for_migration=[
            1,
            2,
            3
        ],
        supported=[
            1,
            2,
            3
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



