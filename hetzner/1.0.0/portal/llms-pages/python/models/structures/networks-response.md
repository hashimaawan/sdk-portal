# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Any.*


# Class Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/meta.md) | Optional | - |
| `networks` | [`List[Network]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/network.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.network import Network
from hetznercloudapi.models.networks_response import NetworksResponse
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.protection_11 import Protection11
from hetznercloudapi.models.route import Route
from hetznercloudapi.models.subnet import Subnet
from hetznercloudapi.models.type_42 import Type42

networks_response = NetworksResponse(
    networks=[
        Network(
            created='2016-01-30T23:50:00+00:00',
            id=4711,
            ip_range='10.0.0.0/16',
            labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
            name='mynet',
            protection=Protection11(
                delete=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            routes=[
                Route(
                    destination='10.100.1.0/24',
                    gateway='10.0.1.1',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            servers=[
                42
            ],
            subnets=[
                Subnet(
                    gateway='10.0.0.1',
                    network_zone='eu-central',
                    mtype=Type42.CLOUD,
                    ip_range='10.0.1.0/24',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            load_balancers=[
                42
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



