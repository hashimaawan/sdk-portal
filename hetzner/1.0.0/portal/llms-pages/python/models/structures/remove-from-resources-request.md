# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `remove_from` | [`List[FirewallRemoveFromResources]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.firewall_remove_from_resources import FirewallRemoveFromResources
from hetznercloudapi.models.label_selector_5 import LabelSelector5
from hetznercloudapi.models.remove_from_resources_request import RemoveFromResourcesRequest
from hetznercloudapi.models.server_9 import Server9
from hetznercloudapi.models.type_7 import Type7

remove_from_resources_request = RemoveFromResourcesRequest(
    remove_from=[
        FirewallRemoveFromResources(
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
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



