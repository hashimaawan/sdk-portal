# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Any.*


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/iso.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.iso import Iso
from hetznercloudapi.models.isos_response_1 import IsosResponse1
from hetznercloudapi.models.type_26 import Type26

isos_response_1 = IsosResponse1(
    iso=Iso(
        deprecated='2018-02-28T00:00:00+00:00',
        description='FreeBSD 11.0 x64',
        id=42,
        name='FreeBSD-11.0-RELEASE-amd64-dvd1',
        mtype=Type26.PUBLIC,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



