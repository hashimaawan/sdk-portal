# Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFsZ29yaXRobQ

Algorithm of the Load Balancer

*This model accepts additional fields of type Any.*


# Class Name

`Algorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mtype` | [`Type28`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-28.md) | Required | Type of the algorithm |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.algorithm import Algorithm
from hetznercloudapi.models.type_28 import Type28

algorithm = Algorithm(
    mtype=Type28.ROUND_ROBIN,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



