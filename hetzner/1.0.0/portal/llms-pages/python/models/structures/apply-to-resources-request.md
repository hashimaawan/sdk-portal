# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apply_to` | [`List[FirewallApplyToResources]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to |


# Example

```python
from hetznercloudapi.models.apply_to_resources_request import ApplyToResourcesRequest
from hetznercloudapi.models.firewall_apply_to_resources import FirewallApplyToResources
from hetznercloudapi.models.label_selector_5 import LabelSelector5
from hetznercloudapi.models.server_9 import Server9
from hetznercloudapi.models.type_7_enum import Type7Enum

apply_to_resources_request = ApplyToResourcesRequest(
    apply_to=[
        FirewallApplyToResources(
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



