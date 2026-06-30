# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | Description of the Image, will be auto-generated if not set |
| `labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `mtype` | [`Type63Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) |


# Example

```python
from hetznercloudapi.models.create_image_request import CreateImageRequest
from hetznercloudapi.models.labels import Labels
from hetznercloudapi.models.type_63_enum import Type63Enum

create_image_request = CreateImageRequest(
    description='my image',
    labels=Labels(
        labelkey='labelkey4'
    ),
    mtype=Type63Enum.SNAPSHOT
)
```



