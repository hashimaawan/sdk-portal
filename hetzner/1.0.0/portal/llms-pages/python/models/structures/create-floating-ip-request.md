# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`CreateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | - |
| `home_location` | `str` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | - |
| `server` | `int` | Optional | Server to assign the Floating IP to |
| `mtype` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-17.md) | Required | Floating IP type |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.create_floating_ip_request import CreateFloatingIpRequest
from hetznercloudapi.models.type_17 import Type17

create_floating_ip_request = CreateFloatingIpRequest(
    mtype=Type17.IPV4,
    description='Web Frontend',
    home_location='fsn1',
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='Web Frontend',
    server=42,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



