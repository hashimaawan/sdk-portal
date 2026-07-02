# V2 Databases Users Reset Auth Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNldCUyNTIwQXV0aCUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesUsersResetAuthRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `mysqlSettings` | [`?MysqlSettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/mysql-settings.md) | Optional | - | getMysqlSettings(): ?MysqlSettings | setMysqlSettings(?MysqlSettings mysqlSettings): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesUsersResetAuthRequestBuilder;
use DigitalOceanApiLib\Models\Builders\MysqlSettingsBuilder;
use DigitalOceanApiLib\Models\AuthPlugin;
use DigitalOceanApiLib\ApiHelper;

$v2DatabasesUsersResetAuthRequest = V2DatabasesUsersResetAuthRequestBuilder::init()
    ->mysqlSettings(
        MysqlSettingsBuilder::init(
            AuthPlugin::MYSQL_NATIVE_PASSWORD
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



