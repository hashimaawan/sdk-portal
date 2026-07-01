# Isos Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`IsosResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isos` | [`List[Iso]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/iso.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/meta.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.iso import Iso
from hetznercloudapi.models.isos_response import IsosResponse
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.type_26 import Type26

isos_response = IsosResponse(
    isos=[
        Iso(
            deprecated='2018-02-28T00:00:00+00:00',
            description='FreeBSD 11.0 x64',
            id=42,
            name='FreeBSD-11.0-RELEASE-amd64-dvd1',
            mtype=Type26.PUBLIC,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



