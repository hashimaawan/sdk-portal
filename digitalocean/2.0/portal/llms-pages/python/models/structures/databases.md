# Databases

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFiYXNlcw

Tagged Resource Statistics include metadata regarding the resource type that has been tagged.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Databases`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `int` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` |
| `last_tagged_uri` | `str` | Optional | The URI for the last tagged object for this type of resource. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.databases import Databases

databases = Databases(
    count=5,
    last_tagged_uri='https://api.digitalocean.com/v2/images/7555620',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



