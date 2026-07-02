# V2 Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGbG9hdGluZyUyNTIwSXBzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floating_ip` | [`FloatingIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/floating-ip-1.md) | Optional | - |
| `links` | [`Links3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links-3.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.action_1 import Action1
from digitaloceanapi.models.floating_ip_1 import FloatingIp1
from digitaloceanapi.models.links_3 import Links3
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.v_2_floating_ips_response_1 import V2FloatingIpsResponse1

v_2_floating_ips_response_1 = V2FloatingIpsResponse1(
    floating_ip=FloatingIp1(
        droplet=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
        ip='ip2',
        locked=False,
        project_id='0000167e-0000-0000-0000-000000000000',
        region=Region(
            available=False,
            features=[
                'features7',
                'features8',
                'features9'
            ],
            name='name6',
            sizes=[
                'sizes6'
            ],
            slug='slug0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    links=Links3(
        actions=[
            Action1(
                href='href0',
                id=154,
                rel='rel4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        droplets=[
            Action1(
                href='href2',
                id=232,
                rel='rel6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Action1(
                href='href2',
                id=232,
                rel='rel6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



