# V2 Registry Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2RegistryResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `registry` | [`Registry`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/registry.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.registry import Registry
from digitaloceanapi.models.v_2_registry_response import V2RegistryResponse

v_2_registry_response = V2RegistryResponse(
    registry=Registry(
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        name='name2',
        region='region8',
        storage_usage_bytes=50,
        storage_usage_bytes_updated_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



