# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listen_port` | `float` | Required | The listen port of the service you want to delete |


# Example

```python
from hetznercloudapi.models.load_balancers_actions_delete_service_request import LoadBalancersActionsDeleteServiceRequest

load_balancers_actions_delete_service_request = LoadBalancersActionsDeleteServiceRequest(
    listen_port=4711
)
```



