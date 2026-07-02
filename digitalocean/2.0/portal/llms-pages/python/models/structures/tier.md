# Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlRpZXI

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Tier`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `build_seconds` | `str` | Optional | - |
| `egress_bandwidth_bytes` | `str` | Optional | - |
| `name` | `str` | Optional | - |
| `slug` | `str` | Optional | - |
| `storage_bytes` | `str` | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.tier import Tier

tier = Tier(
    build_seconds='233',
    egress_bandwidth_bytes='123',
    name='test',
    slug='test',
    storage_bytes='10000000',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



