# Iso

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRklzbw


# Class Name

`Iso`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `str` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. |
| `description` | `str` | Required | Description of the ISO |
| `id` | `int` | Required | ID of the Resource |
| `name` | `str` | Required | Unique identifier of the ISO. Only set for public ISOs |
| `mtype` | [`Type26Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-26.md) | Required | Type of the ISO |


# Example

```python
from hetznercloudapi.models.iso import Iso
from hetznercloudapi.models.type_26_enum import Type26Enum

iso = Iso(
    deprecated='2018-02-28T00:00:00+00:00',
    description='FreeBSD 11.0 x64',
    id=42,
    name='FreeBSD-11.0-RELEASE-amd64-dvd1',
    mtype=Type26Enum.PUBLIC
)
```



