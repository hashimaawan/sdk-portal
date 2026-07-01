# Iso 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRklzbzI

ISO Image that is attached to this Server. Null if no ISO is attached.

*This model accepts additional fields of type Any.*


# Class Name

`Iso2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `str` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. |
| `description` | `str` | Required | Description of the ISO |
| `id` | `int` | Required | ID of the Resource |
| `name` | `str` | Required | Unique identifier of the ISO. Only set for public ISOs |
| `mtype` | [`Type26`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-26.md) | Required | Type of the ISO |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.iso_2 import Iso2
from hetznercloudapi.models.type_26 import Type26

iso_2 = Iso2(
    deprecated='2018-02-28T00:00:00+00:00',
    description='FreeBSD 11.0 x64',
    id=42,
    name='FreeBSD-11.0-RELEASE-amd64-dvd1',
    mtype=Type26.PUBLIC,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



