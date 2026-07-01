# Load Balancers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New Load Balancer name |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.load_balancers_request import LoadBalancersRequest

load_balancers_request = LoadBalancersRequest(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='new-name',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



