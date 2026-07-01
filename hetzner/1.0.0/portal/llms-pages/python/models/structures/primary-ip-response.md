# Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaW1hcnlJUFJlc3BvbnNl


# Class Name

`PrimaryIPResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `primary_ip` | [`PrimaryIP1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/primary-ip-1.md) | Required | - |


# Example

```python
from hetznercloudapi.models.datacenter_2 import Datacenter2
from hetznercloudapi.models.dns_ptr import DnsPtr
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.primary_ip_1 import PrimaryIP1
from hetznercloudapi.models.primary_ip_response import PrimaryIPResponse
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.server_types import ServerTypes
from hetznercloudapi.models.type_50_enum import Type50Enum

primary_ip_response = PrimaryIPResponse(
    primary_ip=PrimaryIP1(
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
            'key1': 'labels1'
        },
        name='my-resource',
        protection=Protection(
            delete=False
        ),
        mtype=Type50Enum.IPV4
    )
)
```



