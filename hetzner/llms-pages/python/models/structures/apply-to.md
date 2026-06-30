# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkFwcGx5VG8


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `label_selector` | [`LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` |
| `server` | [`Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` |
| `mtype` | [`Type7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-7.md) | Required | Type of the resource |


# Example

```python
from hetznercloudapi.models.apply_to import ApplyTo
from hetznercloudapi.models.label_selector_1 import LabelSelector1
from hetznercloudapi.models.server_2 import Server2
from hetznercloudapi.models.type_7_enum import Type7Enum

apply_to = ApplyTo(
    mtype=Type7Enum.SERVER,
    label_selector=LabelSelector1(
        selector='selector8'
    ),
    server=Server2(
        id=14
    )
)
```



