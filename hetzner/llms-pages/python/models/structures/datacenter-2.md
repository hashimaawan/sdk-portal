# Datacenter 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkRhdGFjZW50ZXIy

Datacenter this Primary IP is located at


# Class Name

`Datacenter2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Required | Description of the Datacenter |
| `id` | `int` | Required | ID of the Resource |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/location.md) | Required | - |
| `name` | `str` | Required | Unique identifier of the Datacenter |
| `server_types` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/server-types.md) | Required | The Server types the Datacenter can handle |


# Example

```python
from hetznercloudapi.models.datacenter_2 import Datacenter2
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.server_types import ServerTypes

datacenter_2 = Datacenter2(
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
        network_zone='eu-central'
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
        ]
    )
)
```



