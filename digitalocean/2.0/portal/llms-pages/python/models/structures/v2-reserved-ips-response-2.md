# V2 Reserved Ips Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBSZXNwb25zZTI

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2ReservedIpsResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reserved_ip` | [`ReservedIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/reserved-ip.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.region import Region
from digitaloceanapi.models.reserved_ip import ReservedIp
from digitaloceanapi.models.v_2_reserved_ips_response_2 import V2ReservedIpsResponse2

v_2_reserved_ips_response_2 = V2ReservedIpsResponse2(
    reserved_ip=ReservedIp(
        droplet=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
        ip='ip6',
        locked=False,
        project_id='00002548-0000-0000-0000-000000000000',
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
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



