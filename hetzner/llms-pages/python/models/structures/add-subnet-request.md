# Add Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkFkZFN1Ym5ldFJlcXVlc3Q


# Class Name

`AddSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `str` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. If the Subnet is of type vSwitch, it also can not overlap with any gateway in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. |
| `network_zone` | `str` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. |
| `mtype` | [`Type42Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-42.md) | Required | Type of Subnetwork |
| `vswitch_id` | `int` | Optional | ID of the robot vSwitch. Must be supplied if the subnet is of type vswitch. |


# Example

```python
from hetznercloudapi.models.add_subnet_request import AddSubnetRequest
from hetznercloudapi.models.type_42_enum import Type42Enum

add_subnet_request = AddSubnetRequest(
    network_zone='eu-central',
    mtype=Type42Enum.SERVER,
    ip_range='10.0.1.0/24',
    vswitch_id=1000
)
```



