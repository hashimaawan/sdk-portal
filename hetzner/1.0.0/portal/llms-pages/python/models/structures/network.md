# Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRk5ldHdvcms

*This model accepts additional fields of type Any.*


# Class Name

`Network`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `str` | Required | Point in time when the Network was created (in ISO-8601 format) |
| `id` | `int` | Required | ID of the Network |
| `ip_range` | `str` | Required | IPv4 prefix of the whole Network |
| `labels` | `Any` | Required | User-defined labels (key-value pairs) |
| `load_balancers` | `List[int]` | Optional | Array of IDs of Load Balancers attached to this Network |
| `name` | `str` | Required | Name of the Network |
| `protection` | [`Protection11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/protection-11.md) | Required | Protection configuration for the Network |
| `routes` | [`List[Route]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/route.md) | Required | Array of routes set in this Network |
| `servers` | `List[int]` | Required | Array of IDs of Servers attached to this Network |
| `subnets` | [`List[Subnet]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/subnet.md) | Required | Array subnets allocated in this Network |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.network import Network
from hetznercloudapi.models.protection_11 import Protection11
from hetznercloudapi.models.route import Route
from hetznercloudapi.models.subnet import Subnet
from hetznercloudapi.models.type_42 import Type42

network = Network(
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
```



