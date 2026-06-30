# Load Balancers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Optional | If true, prevents the Load Balancer from being deleted |


# Example

```python
from hetznercloudapi.models.load_balancers_actions_change_protection_request import LoadBalancersActionsChangeProtectionRequest

load_balancers_actions_change_protection_request = LoadBalancersActionsChangeProtectionRequest(
    delete=True
)
```



