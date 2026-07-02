# V2 Databases Users Reset Auth Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNldCUyNTIwQXV0aCUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesUsersResetAuthRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mysql_settings` | [`MysqlSettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/mysql-settings.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.auth_plugin import AuthPlugin
from digitaloceanapi.models.mysql_settings import MysqlSettings
from digitaloceanapi.models.v_2_databases_users_reset_auth_request import V2DatabasesUsersResetAuthRequest

v_2_databases_users_reset_auth_request = V2DatabasesUsersResetAuthRequest(
    mysql_settings=MysqlSettings(
        auth_plugin=AuthPlugin.MYSQL_NATIVE_PASSWORD,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



