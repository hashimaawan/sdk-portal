# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listen_port` | `float` | Required | The listen port of the service you want to delete |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.load_balancers_actions_delete_service_request import LoadBalancersActionsDeleteServiceRequest

load_balancers_actions_delete_service_request = LoadBalancersActionsDeleteServiceRequest(
    listen_port=4711,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



