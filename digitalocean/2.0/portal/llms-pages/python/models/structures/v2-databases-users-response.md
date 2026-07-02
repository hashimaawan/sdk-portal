# V2 Databases Users Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesUsersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `users` | [`List[User]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/user.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.auth_plugin import AuthPlugin
from digitaloceanapi.models.mysql_settings import MysqlSettings
from digitaloceanapi.models.role import Role
from digitaloceanapi.models.user import User
from digitaloceanapi.models.v_2_databases_users_response import V2DatabasesUsersResponse

v_2_databases_users_response = V2DatabasesUsersResponse(
    users=[
        User(
            name='name6',
            mysql_settings=MysqlSettings(
                auth_plugin=AuthPlugin.MYSQL_NATIVE_PASSWORD,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            password='password0',
            role=Role.PRIMARY,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        User(
            name='name6',
            mysql_settings=MysqlSettings(
                auth_plugin=AuthPlugin.MYSQL_NATIVE_PASSWORD,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            password='password0',
            role=Role.PRIMARY,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        User(
            name='name6',
            mysql_settings=MysqlSettings(
                auth_plugin=AuthPlugin.MYSQL_NATIVE_PASSWORD,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            password='password0',
            role=Role.PRIMARY,
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



