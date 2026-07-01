# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mtype` | [`Type39`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.load_balancers_actions_change_algorithm_request import LoadBalancersActionsChangeAlgorithmRequest
from hetznercloudapi.models.type_39 import Type39

load_balancers_actions_change_algorithm_request = LoadBalancersActionsChangeAlgorithmRequest(
    mtype=Type39.ROUND_ROBIN,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



