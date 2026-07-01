# Firewall Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVtb3ZlRnJvbVJlc291cmNlcw

*This model accepts additional fields of type Any.*


# Class Name

`FirewallRemoveFromResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `label_selector` | [`LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `server` | [`Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `mtype` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-7.md) | Optional | Type of the resource |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.firewall_remove_from_resources import FirewallRemoveFromResources
from hetznercloudapi.models.label_selector_5 import LabelSelector5
from hetznercloudapi.models.server_9 import Server9
from hetznercloudapi.models.type_7 import Type7

firewall_remove_from_resources = FirewallRemoveFromResources(
    label_selector=LabelSelector5(
        selector='selector8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    server=Server9(
        id=14,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    mtype=Type7.SERVER,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



