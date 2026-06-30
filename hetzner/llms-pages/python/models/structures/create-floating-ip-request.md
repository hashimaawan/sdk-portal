# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Class Name

`CreateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | - |
| `home_location` | `str` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | - |
| `server` | `int` | Optional | Server to assign the Floating IP to |
| `mtype` | [`Type17Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-17.md) | Required | Floating IP type |


# Example

```python
import jsonpickle

from hetznercloudapi.models.create_floating_ip_request import CreateFloatingIPRequest
from hetznercloudapi.models.type_17_enum import Type17Enum

create_floating_ip_request = CreateFloatingIPRequest(
    mtype=Type17Enum.IPV4,
    description='Web Frontend',
    home_location='fsn1',
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='Web Frontend',
    server=42
)
```



