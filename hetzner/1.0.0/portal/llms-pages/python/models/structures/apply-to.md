# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFwcGx5VG8

*This model accepts additional fields of type Any.*


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `label_selector` | [`LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` |
| `server` | [`Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` |
| `mtype` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-7.md) | Required | Type of the resource |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.apply_to import ApplyTo
from hetznercloudapi.models.label_selector_1 import LabelSelector1
from hetznercloudapi.models.server_2 import Server2
from hetznercloudapi.models.type_7 import Type7

apply_to = ApplyTo(
    mtype=Type7.SERVER,
    label_selector=LabelSelector1(
        selector='selector8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    server=Server2(
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



