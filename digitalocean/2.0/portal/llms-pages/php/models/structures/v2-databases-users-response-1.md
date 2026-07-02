# V2 Databases Users Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesUsersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `user` | [`User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/user.md) | Required | - | getUser(): User | setUser(User user): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesUsersResponse1Builder;
use DigitalOceanApiLib\Models\Builders\UserBuilder;
use DigitalOceanApiLib\Models\Builders\MysqlSettingsBuilder;
use DigitalOceanApiLib\Models\AuthPlugin;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Role;

$v2DatabasesUsersResponse1 = V2DatabasesUsersResponse1Builder::init(
    UserBuilder::init(
        'app-01'
    )
        ->mysqlSettings(
            MysqlSettingsBuilder::init(
                AuthPlugin::MYSQL_NATIVE_PASSWORD
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->password('jge5lfxtzhx42iff')
        ->role(Role::NORMAL)
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



