# Servers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`ServersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/meta.md) | Optional | - |
| `servers` | [`List[Server18]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-18.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.cpu_type import CpuType
from hetznercloudapi.models.created_from import CreatedFrom
from hetznercloudapi.models.datacenter_6 import Datacenter6
from hetznercloudapi.models.dns_ptr_8 import DnsPtr8
from hetznercloudapi.models.image import Image
from hetznercloudapi.models.ipv_44 import Ipv44
from hetznercloudapi.models.ipv_64 import Ipv64
from hetznercloudapi.models.iso_2 import Iso2
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.os_flavor import OsFlavor
from hetznercloudapi.models.pagination import Pagination
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
from hetznercloudapi.models.servers_response import ServersResponse
from hetznercloudapi.models.status_24 import Status24
from hetznercloudapi.models.status_72 import Status72
from hetznercloudapi.models.status_73 import Status73
from hetznercloudapi.models.storage_type import StorageType
from hetznercloudapi.models.type_22 import Type22
from hetznercloudapi.models.type_26 import Type26

servers_response = ServersResponse(
    servers=[
        Server18(
            backup_window='22-02',
            created='2016-01-30T23:55:00+00:00',
            datacenter=Datacenter6(
                description='Falkenstein DC Park 8',
                id=42,
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
                name='fsn1-dc8',
                server_types=ServerTypes(
                    available=[
                        1,
                        2,
                        3
                    ],
                    available_for_migration=[
                        1,
                        2,
                        3
                    ],
                    supported=[
                        1,
                        2,
                        3
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            id=42,
            image=Image(
                bound_to=None,
                created='2016-01-30T23:55:00+00:00',
                created_from=CreatedFrom(
                    id=1,
                    name='Server',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                deleted=None,
                deprecated='2018-02-28T00:00:00+00:00',
                description='Ubuntu 20.04 Standard 64 bit',
                disk_size=10,
                id=42,
                image_size=2.3,
                labels={
                    'key0': 'labels4'
                },
                name='ubuntu-20.04',
                os_flavor=OsFlavor.UBUNTU,
                os_version='20.04',
                protection=Protection(
                    delete=False,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                status=Status24.UNAVAILABLE,
                mtype=Type22.SNAPSHOT,
                rapid_deploy=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            included_traffic=654321,
            ingoing_traffic=123456,
            iso=Iso2(
                deprecated='2018-02-28T00:00:00+00:00',
                description='FreeBSD 11.0 x64',
                id=42,
                name='FreeBSD-11.0-RELEASE-amd64-dvd1',
                mtype=Type26.PUBLIC,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            labels={
                'key0': 'labels0'
            },
            locked=False,
            name='my-resource',
            outgoing_traffic=123456,
            primary_disk_size=50,
            private_net=[
                PrivateNet4(
                    alias_ips=[
                        'alias_ips4'
                    ],
                    ip='10.0.0.2',
                    mac_address='86:00:ff:2a:7d:e1',
                    network=4711,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            protection=Protection20(
                delete=False,
                rebuild=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            public_net=PublicNet4(
                floating_ips=[
                    478
                ],
                ipv_4=Ipv44(
                    blocked=False,
                    dns_ptr='server01.example.com',
                    ip='1.2.3.4',
                    id=42,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                ipv_6=Ipv64(
                    blocked=False,
                    dns_ptr=[
                        DnsPtr8(
                            dns_ptr='server.example.com',
                            ip='2001:db8::1',
                            additional_properties={
                                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                            }
                        )
                    ],
                    ip='2001:db8::/64',
                    id=42,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                firewalls=[
                    ServerPublicNetFirewall(
                        id=250,
                        status=Status72.APPLIED,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    ServerPublicNetFirewall(
                        id=250,
                        status=Status72.APPLIED,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    )
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            rescue_enabled=False,
            server_type=ServerType1(
                cores=1,
                cpu_type=CpuType.SHARED,
                deprecated=False,
                description='CX11',
                disk=25,
                id=1,
                memory=1,
                name='cx11',
                prices=[
                    Price9(
                        location='fsn1',
                        price_hourly=PriceHourly8(
                            gross='1.1900000000000000',
                            net='1.0000000000',
                            additional_properties={
                                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                            }
                        ),
                        price_monthly=PriceMonthly10(
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
                storage_type=StorageType.LOCAL,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            status=Status73.STARTING,
            load_balancers=[
                128,
                129,
                130
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
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            volumes=[
                177
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



