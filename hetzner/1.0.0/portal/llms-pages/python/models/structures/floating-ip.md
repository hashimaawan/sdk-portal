# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `bool` | Required | Whether the IP is blocked |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `description` | `str` | Required | Description of the Resource |
| `dns_ptr` | [`List[DnsPtr]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `home_location` | [`HomeLocation`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/home-location.md) | Required | Location the Floating IP was created in. Routing is optimized for this Location. |
| `id` | `int` | Required | ID of the Resource |
| `ip` | `str` | Required | IP address |
| `labels` | `Dict[str, str]` | Required | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `server` | `int` | Required | ID of the Server the Floating IP is assigned to, null if it is not assigned at all |
| `mtype` | [`Type16Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-16.md) | Required | Type of the Floating IP |


# Example

```python
from hetznercloudapi.models.dns_ptr import DnsPtr
from hetznercloudapi.models.floating_ip import FloatingIp
from hetznercloudapi.models.home_location import HomeLocation
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.type_16_enum import Type16Enum

floating_ip = FloatingIp(
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
```



