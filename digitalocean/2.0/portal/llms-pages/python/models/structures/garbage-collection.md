# Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkdhcmJhZ2VDb2xsZWN0aW9u

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`GarbageCollection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blobs_deleted` | `int` | Optional | The number of blobs deleted as a result of this garbage collection. |
| `created_at` | `datetime` | Optional | The time the garbage collection was created. |
| `freed_bytes` | `int` | Optional | The number of bytes freed as a result of this garbage collection. |
| `registry_name` | `str` | Optional | The name of the container registry. |
| `status` | [`Status15`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-15.md) | Optional | The current status of this garbage collection. |
| `updated_at` | `datetime` | Optional | The time the garbage collection was last updated. |
| `uuid` | `str` | Optional | A string specifying the UUID of the garbage collection. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.garbage_collection import GarbageCollection
from digitaloceanapi.models.status_15 import Status15

garbage_collection = GarbageCollection(
    blobs_deleted=42,
    created_at=dateutil.parser.parse('2020-10-30T21:03:24Z'),
    freed_bytes=667,
    registry_name='example',
    status=Status15.REQUESTED,
    updated_at=dateutil.parser.parse('2020-10-30T21:03:44Z'),
    uuid='eff0feee-49c7-4e8f-ba5c-a320c109c8a8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



