# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `destination_port` | `int` | Required | Port the Load Balancer will balance to |
| `health_check` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-service-health-check.md) | Required | Service health check |
| `http` | [`LoadBalancerServiceHTTP`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https |
| `listen_port` | `int` | Required | Port the Load Balancer listens on |
| `protocol` | [`Protocol7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer |
| `proxyprotocol` | `bool` | Required | Is Proxyprotocol enabled or not |


# Example

```python
from hetznercloudapi.models.http import Http
from hetznercloudapi.models.load_balancer_service import LoadBalancerService
from hetznercloudapi.models.load_balancer_service_health_check import LoadBalancerServiceHealthCheck
from hetznercloudapi.models.load_balancer_service_http import LoadBalancerServiceHTTP
from hetznercloudapi.models.protocol_6_enum import Protocol6Enum
from hetznercloudapi.models.protocol_7_enum import Protocol7Enum

load_balancer_service = LoadBalancerService(
    destination_port=80,
    health_check=LoadBalancerServiceHealthCheck(
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
    ),
    listen_port=443,
    protocol=Protocol7Enum.HTTPS,
    proxyprotocol=False,
    http=LoadBalancerServiceHTTP(
        certificates=[
            180
        ],
        cookie_lifetime=160,
        cookie_name='cookie_name6',
        redirect_http=False,
        sticky_sessions=False
    )
)
```



