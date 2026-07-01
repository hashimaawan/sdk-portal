# Remove Target Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlJlbW92ZVRhcmdldFJlcXVlc3Q


# Class Name

`RemoveTargetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | [`Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `label_selector` | [`LabelSelector12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/label-selector-12.md) | Optional | Configuration for label selector targets, required if type is `label_selector` |
| `server` | [`Server16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-16.md) | Optional | Configuration for type Server, required if type is `server` |
| `mtype` | [`Type29Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-29.md) | Required | Type of the resource |


# Example

```python
from hetznercloudapi.models.ip import Ip
from hetznercloudapi.models.label_selector_12 import LabelSelector12
from hetznercloudapi.models.remove_target_request import RemoveTargetRequest
from hetznercloudapi.models.server_16 import Server16
from hetznercloudapi.models.type_29_enum import Type29Enum

remove_target_request = RemoveTargetRequest(
    mtype=Type29Enum.SERVER,
    ip=Ip(
        ip='ip8'
    ),
    label_selector=LabelSelector12(
        selector='selector8'
    ),
    server=Server16(
        id=217.74
    )
)
```



