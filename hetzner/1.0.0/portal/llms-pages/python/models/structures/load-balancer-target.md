# Load Balancer Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldA

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancerTarget`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `health_status` | [`List[HealthStatus]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/health-status.md) | Optional | List of health statuses of the services on this target |
| `ip` | [`Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `label_selector` | [`LabelSelector7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/label-selector-7.md) | Optional | Label selector and a list of selected targets |
| `server` | [`LoadBalancerTargetServer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-target-server.md) | Optional | Server where the traffic should be routed through |
| `targets` | [`List[Target]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/target.md) | Optional | List of selected targets |
| `mtype` | [`Type29`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-29.md) | Required | Type of the resource |
| `use_private_ip` | `bool` | Optional | Use the private network IP instead of the public IP. Default value is false. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.health_status import HealthStatus
from hetznercloudapi.models.ip import Ip
from hetznercloudapi.models.label_selector_7 import LabelSelector7
from hetznercloudapi.models.load_balancer_target import LoadBalancerTarget
from hetznercloudapi.models.load_balancer_target_server import LoadBalancerTargetServer
from hetznercloudapi.models.server_11 import Server11
from hetznercloudapi.models.status_30 import Status30
from hetznercloudapi.models.target import Target
from hetznercloudapi.models.type_29 import Type29

load_balancer_target = LoadBalancerTarget(
    mtype=Type29.SERVER,
    health_status=[
        HealthStatus(
            listen_port=142,
            status=Status30.UNKNOWN,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        HealthStatus(
            listen_port=142,
            status=Status30.UNKNOWN,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        HealthStatus(
            listen_port=142,
            status=Status30.UNKNOWN,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    ip=Ip(
        ip='ip8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    label_selector=LabelSelector7(
        selector='selector8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    server=LoadBalancerTargetServer(
        id=14,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    targets=[
        Target(
            health_status=[
                HealthStatus(
                    listen_port=142,
                    status=Status30.UNKNOWN,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                HealthStatus(
                    listen_port=142,
                    status=Status30.UNKNOWN,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            server=Server11(
                id=14,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            mtype='type2',
            use_private_ip=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



