# Servers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMg


# Class Name

`ServersResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/server-18.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.cpu_type_enum import CpuTypeEnum
from hetznercloudapi.models.created_from import CreatedFrom
from hetznercloudapi.models.datacenter_6 import Datacenter6
from hetznercloudapi.models.dns_ptr_8 import DnsPtr8
from hetznercloudapi.models.image import Image
from hetznercloudapi.models.ipv_44 import Ipv44
from hetznercloudapi.models.ipv_64 import Ipv64
from hetznercloudapi.models.iso_2 import Iso2
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.os_flavor_enum import OsFlavorEnum
from hetznercloudapi.models.placement_group_nullable import PlacementGroupNullable
from hetznercloudapi.models.price_9 import Price9
from hetznercloudapi.models.price_hourly_8 import PriceHourly8
from hetznercloudapi.models.price_monthly_10 import PriceMonthly10
from hetznercloudapi.models.private_net_4 import PrivateNet4
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.protection_20 import Protection20
from hetznercloudapi.models.public_net_4 import PublicNet4
from hetznercloudapi.models.server_18 import Server18
from hetznercloudapi.models.server_public_net_firewall import ServerPublicNetFirewall
from hetznercloudapi.models.server_type_1 import ServerType1
from hetznercloudapi.models.server_types import ServerTypes
from hetznercloudapi.models.servers_response_2 import ServersResponse2
from hetznercloudapi.models.status_24_enum import Status24Enum
from hetznercloudapi.models.status_72_enum import Status72Enum
from hetznercloudapi.models.status_73_enum import Status73Enum
from hetznercloudapi.models.storage_type_enum import StorageTypeEnum
from hetznercloudapi.models.type_22_enum import Type22Enum
from hetznercloudapi.models.type_26_enum import Type26Enum

servers_response_2 = ServersResponse2(
    server=Server18(
        backup_window='backup_window2',
        created='created4',
        datacenter=Datacenter6(
            description='description0',
            id=200,
            location=Location(
                city='city6',
                country='country8',
                description='description6',
                id=187.14,
                latitude=194.62,
                longitude=59.18,
                name='name4',
                network_zone='network_zone2'
            ),
            name='name0',
            server_types=ServerTypes(
                available=[
                    23.74
                ],
                available_for_migration=[
                    201.65,
                    201.66
                ],
                supported=[
                    69.52,
                    69.53,
                    69.54
                ]
            )
        ),
        id=14,
        image=Image(
            bound_to=186,
            created='created6',
            created_from=CreatedFrom(
                id=60,
                name='name6'
            ),
            deleted='deleted4',
            deprecated='deprecated8',
            description='description6',
            disk_size=244.18,
            id=128,
            image_size=141.34,
            labels={
                'key0': 'labels4'
            },
            name='name6',
            os_flavor=OsFlavorEnum.DEBIAN,
            os_version='os_version4',
            protection=Protection(
                delete=False
            ),
            status=Status24Enum.UNAVAILABLE,
            mtype=Type22Enum.APP,
            rapid_deploy=False
        ),
        included_traffic=123.68,
        ingoing_traffic=151.82,
        iso=Iso2(
            deprecated='deprecated0',
            description='description2',
            id=66,
            name='name8',
            mtype=Type26Enum.PUBLIC
        ),
        labels={
            'key0': 'labels0',
            'key1': 'labels9'
        },
        locked=False,
        name='name4',
        outgoing_traffic=129.6,
        primary_disk_size=19.88,
        private_net=[
            PrivateNet4(
                alias_ips=[
                    'alias_ips4'
                ],
                ip='ip6',
                mac_address='mac_address0',
                network=154
            ),
            PrivateNet4(
                alias_ips=[
                    'alias_ips4'
                ],
                ip='ip6',
                mac_address='mac_address0',
                network=154
            )
        ],
        protection=Protection20(
            delete=False,
            rebuild=False
        ),
        public_net=PublicNet4(
            floating_ips=[
                54,
                55,
                56
            ],
            ipv_4=Ipv44(
                blocked=False,
                dns_ptr='dns_ptr4',
                ip='ip2',
                id=104
            ),
            ipv_6=Ipv64(
                blocked=False,
                dns_ptr=[
                    DnsPtr8(
                        dns_ptr='dns_ptr0',
                        ip='ip6'
                    ),
                    DnsPtr8(
                        dns_ptr='dns_ptr0',
                        ip='ip6'
                    )
                ],
                ip='ip0',
                id=8
            ),
            firewalls=[
                ServerPublicNetFirewall(
                    id=250,
                    status=Status72Enum.APPLIED
                ),
                ServerPublicNetFirewall(
                    id=250,
                    status=Status72Enum.APPLIED
                )
            ]
        ),
        rescue_enabled=False,
        server_type=ServerType1(
            cores=12.84,
            cpu_type=CpuTypeEnum.SHARED,
            deprecated=False,
            description='description0',
            disk=14.32,
            id=30,
            memory=21.2,
            name='name0',
            prices=[
                Price9(
                    location='location8',
                    price_hourly=PriceHourly8(
                        gross='gross4',
                        net='net2'
                    ),
                    price_monthly=PriceMonthly10(
                        gross='gross2',
                        net='net0'
                    )
                )
            ],
            storage_type=StorageTypeEnum.LOCAL
        ),
        status=Status73Enum.STARTING,
        load_balancers=[
            144,
            143,
            142
        ],
        placement_group=PlacementGroupNullable(
            created='created8',
            id=236,
            labels={
                'key0': 'labels4'
            },
            name='name8',
            servers=[
                251,
                252,
                253
            ]
        ),
        volumes=[
            91,
            92
        ]
    )
)
```



