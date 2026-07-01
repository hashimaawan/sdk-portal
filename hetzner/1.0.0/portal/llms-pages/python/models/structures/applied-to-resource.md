# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl

*This model accepts additional fields of type Any.*


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server.md) | Optional | - |
| `mtype` | [`Type5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-5.md) | Optional | Type of resource referenced |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.applied_to_resource import AppliedToResource
from hetznercloudapi.models.server import Server
from hetznercloudapi.models.type_5 import Type5

applied_to_resource = AppliedToResource(
    server=Server(
        id=14,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    mtype=Type5.SERVER,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



