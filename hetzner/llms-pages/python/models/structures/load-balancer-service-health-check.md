# Load Balancer Service Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIZWFsdGhDaGVjaw

Service health check


# Class Name

`LoadBalancerServiceHealthCheck`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `http` | [`Http`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/http.md) | Optional | Additional configuration for protocol http |
| `interval` | `int` | Required | Time interval in seconds health checks are performed |
| `port` | `int` | Required | Port the health check will be performed on |
| `protocol` | [`Protocol6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/protocol-6.md) | Required | Type of the health check |
| `retries` | `int` | Required | Unsuccessful retries needed until a target is considered unhealthy; an unhealthy target needs the same number of successful retries to become healthy again |
| `timeout` | `int` | Required | Time in seconds after an attempt is considered a timeout |


# Example

```python
from hetznercloudapi.models.http import Http
from hetznercloudapi.models.load_balancer_service_health_check import LoadBalancerServiceHealthCheck
from hetznercloudapi.models.protocol_6_enum import Protocol6Enum

load_balancer_service_health_check = LoadBalancerServiceHealthCheck(
    interval=15,
    port=4711,
    protocol=Protocol6Enum.HTTP,
    retries=3,
    timeout=10,
    http=Http(
        domain='domain4',
        path='path2',
        response='response8',
        status_codes=[
            'status_codes0',
            'status_codes1',
            'status_codes2'
        ],
        tls=False
    )
)
```



