# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q


# Class Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mtype` | [`Type39Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer |


# Example

```python
from hetznercloudapi.models.load_balancers_actions_change_algorithm_request import LoadBalancersActionsChangeAlgorithmRequest
from hetznercloudapi.models.type_39_enum import Type39Enum

load_balancers_actions_change_algorithm_request = LoadBalancersActionsChangeAlgorithmRequest(
    mtype=Type39Enum.ROUND_ROBIN
)
```



