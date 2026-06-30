# Primary I Ps Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByaW1hcnlJUHNSZXNwb25zZQ


# Class Name

`PrimaryIPsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/meta.md) | Optional | - |
| `primary_ips` | [`List[PrimaryIP1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/primary-ip-1.md) | Required | - |


# Example

```python
from hetznercloudapi.models.datacenter_2 import Datacenter2
from hetznercloudapi.models.dns_ptr import DnsPtr
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.primary_i_ps_response import PrimaryIPsResponse
from hetznercloudapi.models.primary_ip_1 import PrimaryIP1
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.server_types import ServerTypes
from hetznercloudapi.models.type_50_enum import Type50Enum

primary_i_ps_response = PrimaryIPsResponse(
    primary_ips=[
        PrimaryIP1(
            assignee_id=17,
            auto_delete=True,
            blocked=False,
            created='2016-01-30T23:55:00+00:00',
            datacenter=Datacenter2(
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
            dns_ptr=[
                DnsPtr(
                    dns_ptr='server.example.com',
                    ip='2001:db8::1'
                )
            ],
            id=42,
            ip='131.232.99.1',
            labels={
                'key0': 'labels2',
                'key1': 'labels3',
                'key2': 'labels4'
            },
            name='my-resource',
            protection=Protection(
                delete=False
            ),
            mtype=Type50Enum.IPV4
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64
        )
    )
)
```



