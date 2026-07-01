# Load Balancer Target Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldFNlcnZlcg

Server where the traffic should be routed through

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancerTargetServer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Server |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.load_balancer_target_server import LoadBalancerTargetServer

load_balancer_target_server = LoadBalancerTargetServer(
    id=80,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



