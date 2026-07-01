# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | New description of Image |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `mtype` | [`Type24Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-24.md) | Optional | Destination Image type to convert to |


# Example

```python
import jsonpickle

from hetznercloudapi.models.type_24_enum import Type24Enum
from hetznercloudapi.models.update_image_request import UpdateImageRequest

update_image_request = UpdateImageRequest(
    description='My new Image description',
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    mtype=Type24Enum.SNAPSHOT
)
```



