# Mongodb 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRk1vbmdvZGIx

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Mongodb1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `end_of_availability` | `str` | Optional | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. |
| `end_of_life` | `str` | Optional | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. |
| `version` | `str` | Optional | The engine version. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.mongodb_1 import Mongodb1

mongodb_1 = Mongodb1(
    end_of_availability='2023-05-09T00:00:00Z',
    end_of_life='2023-11-09T00:00:00Z',
    version='8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



