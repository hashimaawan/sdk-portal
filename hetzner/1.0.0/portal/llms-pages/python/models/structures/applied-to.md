# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFwcGxpZWRUbw

*This model accepts additional fields of type Any.*


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applied_to_resources` | [`List[AppliedToResource]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/applied-to-resource.md) | Optional | - |
| `label_selector` | [`LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/label-selector.md) | Optional | - |
| `server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server.md) | Optional | - |
| `mtype` | [`Type6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-6.md) | Required | Type of resource referenced |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.applied_to import AppliedTo
from hetznercloudapi.models.applied_to_resource import AppliedToResource
from hetznercloudapi.models.label_selector import LabelSelector
from hetznercloudapi.models.server import Server
from hetznercloudapi.models.type_5 import Type5
from hetznercloudapi.models.type_6 import Type6

applied_to = AppliedTo(
    mtype=Type6.SERVER,
    applied_to_resources=[
        AppliedToResource(
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
    ],
    label_selector=LabelSelector(
        selector='selector8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    server=Server(
        id=14,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



