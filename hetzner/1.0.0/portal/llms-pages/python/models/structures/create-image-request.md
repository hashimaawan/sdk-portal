# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | Description of the Image, will be auto-generated if not set |
| `labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `mtype` | [`Type63`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.create_image_request import CreateImageRequest
from hetznercloudapi.models.labels import Labels
from hetznercloudapi.models.type_63 import Type63

create_image_request = CreateImageRequest(
    description='my image',
    labels=Labels(
        labelkey='labelkey4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    mtype=Type63.SNAPSHOT,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



