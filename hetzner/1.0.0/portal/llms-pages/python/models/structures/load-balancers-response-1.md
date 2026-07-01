# Load Balancers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Required | - |
| `load_balancer` | [`LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.action import Action
from hetznercloudapi.models.algorithm import Algorithm
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.health_status import HealthStatus
from hetznercloudapi.models.http import Http
from hetznercloudapi.models.ip import Ip
from hetznercloudapi.models.ipv_4 import Ipv4
from hetznercloudapi.models.ipv_6 import Ipv6
from hetznercloudapi.models.label_selector_7 import LabelSelector7
from hetznercloudapi.models.load_balancer import LoadBalancer
from hetznercloudapi.models.load_balancer_service import LoadBalancerService
from hetznercloudapi.models.load_balancer_service_health_check import LoadBalancerServiceHealthCheck
from hetznercloudapi.models.load_balancer_service_http import LoadBalancerServiceHttp
from hetznercloudapi.models.load_balancer_target import LoadBalancerTarget
from hetznercloudapi.models.load_balancer_target_server import LoadBalancerTargetServer
from hetznercloudapi.models.load_balancer_type import LoadBalancerType
from hetznercloudapi.models.load_balancers_response_1 import LoadBalancersResponse1
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.price import Price
from hetznercloudapi.models.price_hourly import PriceHourly
from hetznercloudapi.models.price_monthly import PriceMonthly
from hetznercloudapi.models.private_net import PrivateNet
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.protocol_6 import Protocol6
from hetznercloudapi.models.protocol_7 import Protocol7
from hetznercloudapi.models.public_net import PublicNet
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.server_11 import Server11
from hetznercloudapi.models.status import Status
from hetznercloudapi.models.status_30 import Status30
from hetznercloudapi.models.target import Target
from hetznercloudapi.models.type_28 import Type28
from hetznercloudapi.models.type_29 import Type29

load_balancers_response_1 = LoadBalancersResponse1(
    action=Action(
        command='start_server',
        error=Error(
            code='action_failed',
            message='Action failed',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        finished='2016-01-30T23:55:00+00:00',
        id=42,
        progress=100,
        resources=[
            Resource(
                id=42,
                mtype='server',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        started='2016-01-30T23:55:00+00:00',
        status=Status.RUNNING,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    load_balancer=LoadBalancer(
        algorithm=Algorithm(
            mtype=Type28.ROUND_ROBIN,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        created='2016-01-30T23:55:00+00:00',
        id=42,
        included_traffic=10000,
        ingoing_traffic=216,
        labels={
            'key0': 'labels2',
            'key1': 'labels1'
        },
        load_balancer_type=LoadBalancerType(
            deprecated='2016-01-30T23:50:00+00:00',
            description='LB11',
            id=1,
            max_assigned_certificates=10,
            max_connections=20000,
            max_services=5,
            max_targets=25,
            name='lb11',
            prices=[
                Price(
                    location='fsn1',
                    price_hourly=PriceHourly(
                        gross='1.1900000000000000',
                        net='1.0000000000',
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    price_monthly=PriceMonthly(
                        gross='1.1900000000000000',
                        net='1.0000000000',
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        location=Location(
            city='Falkenstein',
            country='DE',
            description='Falkenstein DC Park 1',
            id=1,
            latitude=50.47612,
            longitude=12.370071,
            name='fsn1',
            network_zone='eu-central',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        name='my-resource',
        outgoing_traffic=42,
        private_net=[
            PrivateNet(
                ip='10.0.0.2',
                network=4711,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        protection=Protection(
            delete=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        public_net=PublicNet(
            enabled=False,
            ipv_4=Ipv4(
                dns_ptr='lb1.example.com',
                ip='1.2.3.4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            ipv_6=Ipv6(
                dns_ptr='lb1.example.com',
                ip='2001:db8::1',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        services=[
            LoadBalancerService(
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
        ],
        targets=[
            LoadBalancerTarget(
                mtype=Type29.IP,
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
                    ),
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
                    ),
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
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



