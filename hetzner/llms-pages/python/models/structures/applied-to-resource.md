# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/server.md) | Optional | - |
| `mtype` | [`Type5Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-5.md) | Optional | Type of resource referenced |


# Example

```python
from hetznercloudapi.models.applied_to_resource import AppliedToResource
from hetznercloudapi.models.server import Server
from hetznercloudapi.models.type_5_enum import Type5Enum

applied_to_resource = AppliedToResource(
    server=Server(
        id=14
    ),
    mtype=Type5Enum.SERVER
)
```



