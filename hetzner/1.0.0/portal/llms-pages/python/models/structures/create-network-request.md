# Create Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`CreateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `str` | Required | IP range of the whole network which must span all included subnets. Must be one of the private IPv4 ranges of RFC1918. Minimum network size is /24. We highly recommend that you pick a larger network with a /16 netmask. |
| `labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the network |
| `routes` | [`List[Route]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/route.md) | Optional | Array of routes set in this network. The destination of the route must be one of the private IPv4 ranges of RFC1918. The gateway must be a subnet/IP of the ip_range of the network object. The destination must not overlap with an existing ip_range in any subnets or with any destinations in other routes or with the first IP of the networks ip_range or with 172.31.1.1. The gateway cannot be the first IP of the networks ip_range and also cannot be 172.31.1.1. |
| `subnets` | [`List[Subnet1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/subnet-1.md) | Optional | Array of subnets allocated. |


# Example

```python
from hetznercloudapi.models.create_network_request import CreateNetworkRequest
from hetznercloudapi.models.labels import Labels
from hetznercloudapi.models.route import Route
from hetznercloudapi.models.subnet_1 import Subnet1
from hetznercloudapi.models.type_42_enum import Type42Enum

create_network_request = CreateNetworkRequest(
    ip_range='10.0.0.0/16',
    name='mynet',
    labels=Labels(
        labelkey='labelkey4'
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
    subnets=[
        Subnet1(
            network_zone='network_zone2',
            mtype=Type42Enum.CLOUD,
            ip_range='ip_range6'
        )
    ]
)
```



