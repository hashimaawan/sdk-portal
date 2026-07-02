# V2 Databases Migrate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME1pZ3JhdGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesMigrateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `region` | `str` | Required | A slug identifier for the region to which the database cluster will be migrated. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_databases_migrate_request import V2DatabasesMigrateRequest

v_2_databases_migrate_request = V2DatabasesMigrateRequest(
    region='lon1',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



