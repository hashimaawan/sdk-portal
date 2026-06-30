# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `remove_from` | [`List[FirewallRemoveFromResources]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from |


# Example

```python
from hetznercloudapi.models.firewall_remove_from_resources import FirewallRemoveFromResources
from hetznercloudapi.models.label_selector_5 import LabelSelector5
from hetznercloudapi.models.remove_from_resources_request import RemoveFromResourcesRequest
from hetznercloudapi.models.server_9 import Server9
from hetznercloudapi.models.type_7_enum import Type7Enum

remove_from_resources_request = RemoveFromResourcesRequest(
    remove_from=[
        FirewallRemoveFromResources(
            label_selector=LabelSelector5(
                selector='selector8'
            ),
            server=Server9(
                id=14
            ),
            mtype=Type7Enum.SERVER
        )
    ]
)
```



