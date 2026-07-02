# V2 Reserved Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2ReservedIpsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reserved_ips` | [`List[ReservedIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/reserved-ip.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.reserved_ip import ReservedIp
from digitaloceanapi.models.v_2_reserved_ips_response import V2ReservedIpsResponse

v_2_reserved_ips_response = V2ReservedIpsResponse(
    meta=Meta(
        total=1,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    reserved_ips=[
        ReservedIp(
            droplet=None,
            ip='45.55.96.47',
            locked=False,
            project_id='746c6152-2fa2-11ed-92d3-27aaa54e4988',
            region=Region(
                available=True,
                features=[
                    'private_networking',
                    'backups',
                    'ipv6',
                    'metadata',
                    'install_agent',
                    'storage',
                    'image_transfer'
                ],
                name='New York 3',
                sizes=[
                    's-1vcpu-1gb',
                    's-1vcpu-2gb',
                    's-1vcpu-3gb',
                    's-2vcpu-2gb',
                    's-3vcpu-1gb',
                    's-2vcpu-4gb',
                    's-4vcpu-8gb',
                    's-6vcpu-16gb',
                    's-8vcpu-32gb',
                    's-12vcpu-48gb',
                    's-16vcpu-64gb',
                    's-20vcpu-96gb',
                    's-24vcpu-128gb',
                    's-32vcpu-192g'
                ],
                slug='nyc3',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='last6',
            next='next2',
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



