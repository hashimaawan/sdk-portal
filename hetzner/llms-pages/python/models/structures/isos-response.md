# Isos Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNl


# Class Name

`IsosResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isos` | [`List[Iso]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/iso.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/meta.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.iso import Iso
from hetznercloudapi.models.isos_response import IsosResponse
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.type_26_enum import Type26Enum

isos_response = IsosResponse(
    isos=[
        Iso(
            deprecated='2018-02-28T00:00:00+00:00',
            description='FreeBSD 11.0 x64',
            id=42,
            name='FreeBSD-11.0-RELEASE-amd64-dvd1',
            mtype=Type26Enum.PUBLIC
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64
        )
    )
)
```



