# Load Balancers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVxdWVzdA


# Class Name

`LoadBalancersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New Load Balancer name |


# Example

```python
import jsonpickle

from hetznercloudapi.models.load_balancers_request import LoadBalancersRequest

load_balancers_request = LoadBalancersRequest(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='new-name'
)
```



