# V2 Databases Online Migration Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesOnlineMigrationResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `str` | Optional | The time the migration was initiated, in ISO 8601 format. |
| `id` | `str` | Optional | The ID of the most recent migration. |
| `status` | [`Status5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-5.md) | Optional | The current status of the migration. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.status_5 import Status5
from digitaloceanapi.models.v_2_databases_online_migration_response import V2DatabasesOnlineMigrationResponse

v_2_databases_online_migration_response = V2DatabasesOnlineMigrationResponse(
    created_at='2020-10-29T15:57:38Z',
    id='77b28fc8-19ff-11eb-8c9c-c68e24557488',
    status=Status5.RUNNING,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



