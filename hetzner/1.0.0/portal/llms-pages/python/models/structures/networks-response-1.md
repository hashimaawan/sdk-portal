# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | [`Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/network.md) | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.network import Network
from hetznercloudapi.models.networks_response_1 import NetworksResponse1
from hetznercloudapi.models.protection_11 import Protection11
from hetznercloudapi.models.route import Route
from hetznercloudapi.models.subnet import Subnet
from hetznercloudapi.models.type_42_enum import Type42Enum

networks_response_1 = NetworksResponse1(
    network=Network(
        created='created4',
        id=78,
        ip_range='ip_range6',
        labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
        name='name4',
        protection=Protection11(
            delete=False
        ),
        routes=[
            Route(
                destination='destination8',
                gateway='gateway6'
            ),
            Route(
                destination='destination8',
                gateway='gateway6'
            ),
            Route(
                destination='destination8',
                gateway='gateway6'
            )
        ],
        servers=[
            93
        ],
        subnets=[
            Subnet(
                gateway='gateway4',
                network_zone='network_zone2',
                mtype=Type42Enum.CLOUD,
                ip_range='ip_range6'
            )
        ],
        load_balancers=[
            208
        ]
    )
)
```



