# Load Balancers Actions Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQXR0YWNoJTI1MjBUbyUyNTIwTmV0d29yayUyNTIwUmVxdWVzdA


# Class Name

`LoadBalancersActionsAttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | `str` | Optional | IP to request to be assigned to this Load Balancer; if you do not provide this then you will be auto assigned an IP address |
| `network` | `float` | Required | ID of an existing network to attach the Load Balancer to |


# Example

```python
from hetznercloudapi.models.load_balancers_actions_attach_to_network_request import LoadBalancersActionsAttachToNetworkRequest

load_balancers_actions_attach_to_network_request = LoadBalancersActionsAttachToNetworkRequest(
    network=4711,
    ip='10.0.1.1'
)
```



