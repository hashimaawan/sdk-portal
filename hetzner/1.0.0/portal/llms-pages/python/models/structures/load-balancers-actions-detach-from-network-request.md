# Load Balancers Actions Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGV0YWNoJTI1MjBGcm9tJTI1MjBOZXR3b3JrJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `float` | Required | ID of an existing network to detach the Load Balancer from |


# Example

```python
from hetznercloudapi.models.load_balancers_actions_detach_from_network_request import LoadBalancersActionsDetachFromNetworkRequest

load_balancers_actions_detach_from_network_request = LoadBalancersActionsDetachFromNetworkRequest(
    network=4711
)
```



