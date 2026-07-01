# Load Balancers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2Uy


# Class Name

`LoadBalancersResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer` | [`LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer.md) | Required | - |


# Example

```python
from hetznercloudapi.models.algorithm import Algorithm
from hetznercloudapi.models.health_status import HealthStatus
from hetznercloudapi.models.http import Http
from hetznercloudapi.models.ip import Ip
from hetznercloudapi.models.ipv_4 import Ipv4
from hetznercloudapi.models.ipv_6 import Ipv6
from hetznercloudapi.models.label_selector_7 import LabelSelector7
from hetznercloudapi.models.load_balancer import LoadBalancer
from hetznercloudapi.models.load_balancer_service import LoadBalancerService
from hetznercloudapi.models.load_balancer_service_health_check import LoadBalancerServiceHealthCheck
from hetznercloudapi.models.load_balancer_service_http import LoadBalancerServiceHTTP
from hetznercloudapi.models.load_balancer_target import LoadBalancerTarget
from hetznercloudapi.models.load_balancer_target_server import LoadBalancerTargetServer
from hetznercloudapi.models.load_balancer_type import LoadBalancerType
from hetznercloudapi.models.load_balancers_response_2 import LoadBalancersResponse2
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.price import Price
from hetznercloudapi.models.price_hourly import PriceHourly
from hetznercloudapi.models.price_monthly import PriceMonthly
from hetznercloudapi.models.private_net import PrivateNet
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.protocol_6_enum import Protocol6Enum
from hetznercloudapi.models.protocol_7_enum import Protocol7Enum
from hetznercloudapi.models.public_net import PublicNet
from hetznercloudapi.models.server_11 import Server11
from hetznercloudapi.models.status_30_enum import Status30Enum
from hetznercloudapi.models.target import Target
from hetznercloudapi.models.type_28_enum import Type28Enum
from hetznercloudapi.models.type_29_enum import Type29Enum

load_balancers_response_2 = LoadBalancersResponse2(
    load_balancer=LoadBalancer(
        algorithm=Algorithm(
            mtype=Type28Enum.ROUND_ROBIN
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
                        net='1.0000000000'
                    ),
                    price_monthly=PriceMonthly(
                        gross='1.1900000000000000',
                        net='1.0000000000'
                    )
                )
            ]
        ),
        location=Location(
            city='Falkenstein',
            country='DE',
            description='Falkenstein DC Park 1',
            id=1,
            latitude=50.47612,
            longitude=12.370071,
            name='fsn1',
            network_zone='eu-central'
        ),
        name='my-resource',
        outgoing_traffic=42,
        private_net=[
            PrivateNet(
                ip='10.0.0.2',
                network=4711
            )
        ],
        protection=Protection(
            delete=False
        ),
        public_net=PublicNet(
            enabled=False,
            ipv_4=Ipv4(
                dns_ptr='lb1.example.com',
                ip='1.2.3.4'
            ),
            ipv_6=Ipv6(
                dns_ptr='lb1.example.com',
                ip='2001:db8::1'
            )
        ),
        services=[
            LoadBalancerService(
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
        ],
        targets=[
            LoadBalancerTarget(
                mtype=Type29Enum.IP,
                health_status=[
                    HealthStatus(
                        listen_port=142,
                        status=Status30Enum.UNKNOWN
                    ),
                    HealthStatus(
                        listen_port=142,
                        status=Status30Enum.UNKNOWN
                    )
                ],
                ip=Ip(
                    ip='ip8'
                ),
                label_selector=LabelSelector7(
                    selector='selector8'
                ),
                server=LoadBalancerTargetServer(
                    id=14
                ),
                targets=[
                    Target(
                        health_status=[
                            HealthStatus(
                                listen_port=142,
                                status=Status30Enum.UNKNOWN
                            ),
                            HealthStatus(
                                listen_port=142,
                                status=Status30Enum.UNKNOWN
                            )
                        ],
                        server=Server11(
                            id=14
                        ),
                        mtype='type2',
                        use_private_ip=False
                    ),
                    Target(
                        health_status=[
                            HealthStatus(
                                listen_port=142,
                                status=Status30Enum.UNKNOWN
                            ),
                            HealthStatus(
                                listen_port=142,
                                status=Status30Enum.UNKNOWN
                            )
                        ],
                        server=Server11(
                            id=14
                        ),
                        mtype='type2',
                        use_private_ip=False
                    ),
                    Target(
                        health_status=[
                            HealthStatus(
                                listen_port=142,
                                status=Status30Enum.UNKNOWN
                            ),
                            HealthStatus(
                                listen_port=142,
                                status=Status30Enum.UNKNOWN
                            )
                        ],
                        server=Server11(
                            id=14
                        ),
                        mtype='type2',
                        use_private_ip=False
                    )
                ]
            )
        ]
    )
)
```



