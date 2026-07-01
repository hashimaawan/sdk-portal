# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `destination_port` | `int` | Required | Port the Load Balancer will balance to |
| `health_check` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-service-health-check.md) | Required | Service health check |
| `http` | [`LoadBalancerServiceHttp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https |
| `listen_port` | `int` | Required | Port the Load Balancer listens on |
| `protocol` | [`Protocol7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer |
| `proxyprotocol` | `bool` | Required | Is Proxyprotocol enabled or not |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.http import Http
from hetznercloudapi.models.load_balancer_service import LoadBalancerService
from hetznercloudapi.models.load_balancer_service_health_check import LoadBalancerServiceHealthCheck
from hetznercloudapi.models.load_balancer_service_http import LoadBalancerServiceHttp
from hetznercloudapi.models.protocol_6 import Protocol6
from hetznercloudapi.models.protocol_7 import Protocol7

load_balancer_service = LoadBalancerService(
    destination_port=80,
    health_check=LoadBalancerServiceHealthCheck(
        interval=15,
        port=4711,
        protocol=Protocol6.HTTP,
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
    protocol=Protocol7.HTTPS,
    proxyprotocol=False,
    http=LoadBalancerServiceHttp(
        certificates=[
            180
        ],
        cookie_lifetime=160,
        cookie_name='cookie_name6',
        redirect_http=False,
        sticky_sessions=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



