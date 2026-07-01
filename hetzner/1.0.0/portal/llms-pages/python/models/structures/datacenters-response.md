# Datacenters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Any.*


# Class Name

`DatacentersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datacenters` | [`List[Datacenter]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/datacenter.md) | Required | - |
| `recommendation` | `float` | Required | The Datacenter which is recommended to be used to create new Servers. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

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
    ],
    recommendation=1,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



