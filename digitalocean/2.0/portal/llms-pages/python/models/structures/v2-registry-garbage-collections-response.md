# V2 Registry Garbage Collections Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwR2FyYmFnZSUyNTIwQ29sbGVjdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2RegistryGarbageCollectionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `garbage_collections` | [`List[GarbageCollection]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/garbage-collection.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.garbage_collection import GarbageCollection
from digitaloceanapi.models.status_15 import Status15
from digitaloceanapi.models.v_2_registry_garbage_collections_response import V2RegistryGarbageCollectionsResponse

v_2_registry_garbage_collections_response = V2RegistryGarbageCollectionsResponse(
    garbage_collections=[
        GarbageCollection(
            blobs_deleted=26,
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            freed_bytes=100,
            registry_name='registry_name2',
            status=Status15.REQUESTED,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



