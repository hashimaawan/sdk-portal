# Floating Ips Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMg


# Class Name

`FloatingIpsResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floating_ip` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/floating-ip.md) | Required | - |


# Example

```python
from hetznercloudapi.models.dns_ptr import DnsPtr
from hetznercloudapi.models.floating_ip import FloatingIp
from hetznercloudapi.models.floating_ips_response_2 import FloatingIpsResponse2
from hetznercloudapi.models.home_location import HomeLocation
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.type_16_enum import Type16Enum

floating_ips_response_2 = FloatingIpsResponse2(
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
    )
)
```



