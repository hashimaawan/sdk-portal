# V2 Databases Online Migration Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesOnlineMigrationRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `disable_ssl` | `bool` | Optional | Enables SSL encryption when connecting to the source database. |
| `source` | [`Source`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/source.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.source import Source
from digitaloceanapi.models.v_2_databases_online_migration_request import V2DatabasesOnlineMigrationRequest

v_2_databases_online_migration_request = V2DatabasesOnlineMigrationRequest(
    disable_ssl=False,
    source=Source(
        database='database4',
        host='host4',
        password='password8',
        port=180,
        ssl=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



