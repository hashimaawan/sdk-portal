# Reserved Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlc2VydmVkSXA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`ReservedIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet` | Any \| None \| [Droplet](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/droplet.md) | Optional | This is a container for any-of cases. |
| `ip` | `str` | Optional | The public IP address of the reserved IP. It also serves as its identifier. |
| `locked` | `bool` | Optional | A boolean value indicating whether or not the reserved IP has pending actions preventing new ones from being submitted. |
| `project_id` | `uuid\|str` | Optional | The UUID of the project to which the reserved IP currently belongs. |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/region.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.region import Region
from digitaloceanapi.models.reserved_ip import ReservedIp

reserved_ip = ReservedIp(
    droplet=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    ip='45.55.96.47',
    locked=True,
    project_id='746c6152-2fa2-11ed-92d3-27aaa54e4988',
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
)
```



