# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/iso.md) | Required | - |


# Example

```python
from hetznercloudapi.models.iso import Iso
from hetznercloudapi.models.isos_response_1 import IsosResponse1
from hetznercloudapi.models.type_26_enum import Type26Enum

isos_response_1 = IsosResponse1(
    iso=Iso(
        deprecated='2018-02-28T00:00:00+00:00',
        description='FreeBSD 11.0 x64',
        id=42,
        name='FreeBSD-11.0-RELEASE-amd64-dvd1',
        mtype=Type26Enum.PUBLIC
    )
)
```



