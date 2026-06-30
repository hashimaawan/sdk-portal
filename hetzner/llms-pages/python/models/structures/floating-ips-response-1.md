# Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMQ


# Class Name

`FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/action.md) | Optional | - |
| `floating_ip` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/floating-ip.md) | Required | - |


# Example

```python
from hetznercloudapi.models.action import Action
from hetznercloudapi.models.dns_ptr import DnsPtr
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.floating_ip import FloatingIp
from hetznercloudapi.models.floating_ips_response_1 import FloatingIpsResponse1
from hetznercloudapi.models.home_location import HomeLocation
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status_enum import StatusEnum
from hetznercloudapi.models.type_16_enum import Type16Enum

floating_ips_response_1 = FloatingIpsResponse1(
    floating_ip=FloatingIp(
        blocked=False,
        created='2016-01-30T23:55:00+00:00',
        description='this describes my resource',
        dns_ptr=[
            DnsPtr(
                dns_ptr='server.example.com',
                ip='2001:db8::1'
            )
        ],
        home_location=HomeLocation(
            city='Falkenstein',
            country='DE',
            description='Falkenstein DC Park 1',
            id=1,
            latitude=50.47612,
            longitude=12.370071,
            name='fsn1',
            network_zone='eu-central'
        ),
        id=42,
        ip='131.232.99.1',
        labels={
            'key0': 'labels4',
            'key1': 'labels3',
            'key2': 'labels2'
        },
        name='my-resource',
        protection=Protection(
            delete=False
        ),
        server=42,
        mtype=Type16Enum.IPV4
    ),
    action=Action(
        command='command6',
        error=Error(
            code='code2',
            message='message4'
        ),
        finished='finished0',
        id=238,
        progress=143.26,
        resources=[
            Resource(
                id=198,
                mtype='type0'
            ),
            Resource(
                id=198,
                mtype='type0'
            ),
            Resource(
                id=198,
                mtype='type0'
            )
        ],
        started='started8',
        status=StatusEnum.RUNNING
    )
)
```



