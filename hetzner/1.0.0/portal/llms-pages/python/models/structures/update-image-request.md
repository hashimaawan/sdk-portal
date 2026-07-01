# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | New description of Image |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `mtype` | [`Type24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-24.md) | Optional | Destination Image type to convert to |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.type_24 import Type24
from hetznercloudapi.models.update_image_request import UpdateImageRequest

update_image_request = UpdateImageRequest(
    description='My new Image description',
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    mtype=Type24.SNAPSHOT,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



