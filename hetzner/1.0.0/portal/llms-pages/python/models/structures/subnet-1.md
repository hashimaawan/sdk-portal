# Subnet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlN1Ym5ldDE

*This model accepts additional fields of type Any.*


# Class Name

`Subnet1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `str` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. |
| `network_zone` | `str` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. |
| `mtype` | [`Type42`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-42.md) | Required | Type of Subnetwork |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.subnet_1 import Subnet1
from hetznercloudapi.models.type_42 import Type42

subnet_1 = Subnet1(
    network_zone='eu-central',
    mtype=Type42.CLOUD,
    ip_range='10.0.1.0/24',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



