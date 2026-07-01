# Server 18

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcjE4


# Class Name

`Server18`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backup_window` | `str` | Required | Time window (UTC) in which the backup will run, or null if the backups are not enabled |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `datacenter` | [`Datacenter6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/datacenter-6.md) | Required | Datacenter this Resource is located at |
| `id` | `int` | Required | ID of the Resource |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/image.md) | Required | - |
| `included_traffic` | `float` | Required | Free Traffic for the current billing period in bytes |
| `ingoing_traffic` | `float` | Required | Inbound Traffic for the current billing period in bytes |
| `iso` | [`Iso2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/iso-2.md) | Required | ISO Image that is attached to this Server. Null if no ISO is attached. |
| `labels` | `Dict[str, str]` | Required | User-defined labels (key-value pairs) |
| `load_balancers` | `List[int]` | Optional | - |
| `locked` | `bool` | Required | True if Server has been locked and is not available to user |
| `name` | `str` | Required | Name of the Server (must be unique per Project and a valid hostname as per RFC 1123) |
| `outgoing_traffic` | `float` | Required | Outbound Traffic for the current billing period in bytes |
| `placement_group` | [`PlacementGroupNullable`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/placement-group-nullable.md) | Optional | - |
| `primary_disk_size` | `float` | Required | Size of the primary Disk |
| `private_net` | [`List[PrivateNet4]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/private-net-4.md) | Required | Private networks information |
| `protection` | [`Protection20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/protection-20.md) | Required | Protection configuration for the Server |
| `public_net` | [`PublicNet4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/public-net-4.md) | Required | Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip` |
| `rescue_enabled` | `bool` | Required | True if rescue mode is enabled. Server will then boot into rescue system on next reboot |
| `server_type` | [`ServerType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-type-1.md) | Required | Type of Server - determines how much ram, disk and cpu a Server has |
| `status` | [`Status73Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/status-73.md) | Required | Status of the Server |
| `volumes` | `List[int]` | Optional | IDs of Volumes assigned to this Server |


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
from hetznercloudapi.models.status_24_enum import Status24Enum
from hetznercloudapi.models.status_72_enum import Status72Enum
from hetznercloudapi.models.status_73_enum import Status73Enum
from hetznercloudapi.models.storage_type_enum import StorageTypeEnum
from hetznercloudapi.models.type_22_enum import Type22Enum
from hetznercloudapi.models.type_26_enum import Type26Enum

server_18 = Server18(
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
            network_zone='eu-central'
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
            ]
        )
    ),
    id=42,
    image=Image(
        bound_to=None,
        created='2016-01-30T23:55:00+00:00',
        created_from=CreatedFrom(
            id=1,
            name='Server'
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
        os_flavor=OsFlavorEnum.UBUNTU,
        os_version='20.04',
        protection=Protection(
            delete=False
        ),
        status=Status24Enum.UNAVAILABLE,
        mtype=Type22Enum.SNAPSHOT,
        rapid_deploy=False
    ),
    included_traffic=654321,
    ingoing_traffic=123456,
    iso=Iso2(
        deprecated='2018-02-28T00:00:00+00:00',
        description='FreeBSD 11.0 x64',
        id=42,
        name='FreeBSD-11.0-RELEASE-amd64-dvd1',
        mtype=Type26Enum.PUBLIC
    ),
    labels={
        'key0': 'labels2',
        'key1': 'labels1'
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
            network=4711
        )
    ],
    protection=Protection20(
        delete=False,
        rebuild=False
    ),
    public_net=PublicNet4(
        floating_ips=[
            478
        ],
        ipv_4=Ipv44(
            blocked=False,
            dns_ptr='server01.example.com',
            ip='1.2.3.4',
            id=42
        ),
        ipv_6=Ipv64(
            blocked=False,
            dns_ptr=[
                DnsPtr8(
                    dns_ptr='server.example.com',
                    ip='2001:db8::1'
                )
            ],
            ip='2001:db8::/64',
            id=42
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
        cores=1,
        cpu_type=CpuTypeEnum.SHARED,
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
                    net='1.0000000000'
                ),
                price_monthly=PriceMonthly10(
                    gross='1.1900000000000000',
                    net='1.0000000000'
                )
            )
        ],
        storage_type=StorageTypeEnum.LOCAL
    ),
    status=Status73Enum.RUNNING,
    load_balancers=[
        252
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
        45,
        44,
        43
    ]
)
```



