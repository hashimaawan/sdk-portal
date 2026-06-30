# Datacenters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZQ


# Class Name

`DatacentersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datacenters` | [`List[Datacenter]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/datacenter.md) | Required | - |
| `recommendation` | `float` | Required | The Datacenter which is recommended to be used to create new Servers. |


# Example

```python
from hetznercloudapi.models.datacenter import Datacenter
from hetznercloudapi.models.datacenters_response import DatacentersResponse
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.server_types import ServerTypes

datacenters_response = DatacentersResponse(
    datacenters=[
        Datacenter(
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
    ],
    recommendation=1
)
```



