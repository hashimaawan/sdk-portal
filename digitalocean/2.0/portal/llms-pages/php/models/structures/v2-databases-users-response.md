# V2 Databases Users Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesUsersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `users` | [`?(User[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/user.md) | Optional | - | getUsers(): ?array | setUsers(?array users): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesUsersResponseBuilder;
use DigitalOceanApiLib\Models\Builders\UserBuilder;
use DigitalOceanApiLib\Models\Builders\MysqlSettingsBuilder;
use DigitalOceanApiLib\Models\AuthPlugin;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Role;

$v2DatabasesUsersResponse = V2DatabasesUsersResponseBuilder::init()
    ->users(
        [
            UserBuilder::init(
                'name6'
            )
                ->mysqlSettings(
                    MysqlSettingsBuilder::init(
                        AuthPlugin::MYSQL_NATIVE_PASSWORD
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->password('password0')
                ->role(Role::PRIMARY)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            UserBuilder::init(
                'name6'
            )
                ->mysqlSettings(
                    MysqlSettingsBuilder::init(
                        AuthPlugin::MYSQL_NATIVE_PASSWORD
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->password('password0')
                ->role(Role::PRIMARY)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



