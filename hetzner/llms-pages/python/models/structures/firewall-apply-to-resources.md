# Firewall Apply to Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkZpcmV3YWxsQXBwbHlUb1Jlc291cmNlcw


# Class Name

`FirewallApplyToResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `label_selector` | [`LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `server` | [`Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `mtype` | [`Type7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-7.md) | Optional | Type of the resource |


# Example

```python
from hetznercloudapi.models.firewall_apply_to_resources import FirewallApplyToResources
from hetznercloudapi.models.label_selector_5 import LabelSelector5
from hetznercloudapi.models.server_9 import Server9
from hetznercloudapi.models.type_7_enum import Type7Enum

firewall_apply_to_resources = FirewallApplyToResources(
    label_selector=LabelSelector5(
        selector='selector8'
    ),
    server=Server9(
        id=14
    ),
    mtype=Type7Enum.SERVER
)
```



