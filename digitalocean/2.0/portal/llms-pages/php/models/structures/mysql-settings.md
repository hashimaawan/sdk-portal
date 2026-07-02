# Mysql Settings

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk15c3FsU2V0dGluZ3M

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`MysqlSettings`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `authPlugin` | [`string(AuthPlugin)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/auth-plugin.md) | Required | A string specifying the authentication method to be used for connections<br>to the MySQL user account. The valid values are `mysql_native_password`<br>or `caching_sha2_password`. If excluded when creating a new user, the<br>default for the version of MySQL in use will be used. As of MySQL 8.0, the<br>default is `caching_sha2_password`. | getAuthPlugin(): string | setAuthPlugin(string authPlugin): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\MysqlSettingsBuilder;
use DigitalOceanApiLib\Models\AuthPlugin;
use DigitalOceanApiLib\ApiHelper;

$mysqlSettings = MysqlSettingsBuilder::init(
    AuthPlugin::MYSQL_NATIVE_PASSWORD
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



