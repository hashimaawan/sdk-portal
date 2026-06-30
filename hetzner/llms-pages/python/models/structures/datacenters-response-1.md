# Datacenters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZTE


# Class Name

`DatacentersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datacenter` | [`Datacenter`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/datacenter.md) | Required | - |


# Example

```python
from hetznercloudapi.models.datacenter import Datacenter
from hetznercloudapi.models.datacenters_response_1 import DatacentersResponse1
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.server_types import ServerTypes

datacenters_response_1 = DatacentersResponse1(
    datacenter=Datacenter(
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
)
```



