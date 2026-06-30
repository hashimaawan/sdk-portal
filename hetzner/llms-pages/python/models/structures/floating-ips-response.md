# Floating Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floating_ips` | [`List[FloatingIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/floating-ip.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/meta.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.dns_ptr import DnsPtr
from hetznercloudapi.models.floating_ip import FloatingIp
from hetznercloudapi.models.floating_ips_response import FloatingIpsResponse
from hetznercloudapi.models.home_location import HomeLocation
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.type_16_enum import Type16Enum

floating_ips_response = FloatingIpsResponse(
    floating_ips=[
        FloatingIp(
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
                'key0': 'labels2'
            },
            name='my-resource',
            protection=Protection(
                delete=False
            ),
            server=42,
            mtype=Type16Enum.IPV4
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



