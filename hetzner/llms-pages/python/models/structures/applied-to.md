# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkFwcGxpZWRUbw


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applied_to_resources` | [`List[AppliedToResource]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/applied-to-resource.md) | Optional | - |
| `label_selector` | [`LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/label-selector.md) | Optional | - |
| `server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/server.md) | Optional | - |
| `mtype` | [`Type6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-6.md) | Required | Type of resource referenced |


# Example

```python
from hetznercloudapi.models.applied_to import AppliedTo
from hetznercloudapi.models.applied_to_resource import AppliedToResource
from hetznercloudapi.models.label_selector import LabelSelector
from hetznercloudapi.models.server import Server
from hetznercloudapi.models.type_5_enum import Type5Enum
from hetznercloudapi.models.type_6_enum import Type6Enum

applied_to = AppliedTo(
    mtype=Type6Enum.SERVER,
    applied_to_resources=[
        AppliedToResource(
            server=Server(
                id=14
            ),
            mtype=Type5Enum.SERVER
        )
    ],
    label_selector=LabelSelector(
        selector='selector8'
    ),
    server=Server(
        id=14
    )
)
```



