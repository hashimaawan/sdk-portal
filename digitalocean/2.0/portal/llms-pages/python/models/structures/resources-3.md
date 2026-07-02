# Resources 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlc291cmNlczM

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Resources3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_id` | `str` | Optional | The identifier of a resource. |
| `resource_type` | [`ResourceType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/resource-type-2.md) | Optional | The type of the resource. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.resource_type_2 import ResourceType2
from digitaloceanapi.models.resources_3 import Resources3

resources_3 = Resources3(
    resource_id='3d80cb72-342b-4aaa-b92e-4e4abb24a933',
    resource_type=ResourceType2.VOLUME,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



