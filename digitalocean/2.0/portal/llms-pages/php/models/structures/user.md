# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlVzZXI

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`User`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `mysqlSettings` | [`?MysqlSettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/mysql-settings.md) | Optional | - | getMysqlSettings(): ?MysqlSettings | setMysqlSettings(?MysqlSettings mysqlSettings): void |
| `name` | `string` | Required | The name of a database user. | getName(): string | setName(string name): void |
| `password` | `?string` | Optional, Read-only | A randomly generated password for the database user. | getPassword(): ?string | setPassword(?string password): void |
| `role` | [`?string(Role)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/role.md) | Optional, Read-only | A string representing the database user's role. The value will be either<br>"primary" or "normal". | getRole(): ?string | setRole(?string role): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\UserBuilder;
use DigitalOceanApiLib\Models\Builders\MysqlSettingsBuilder;
use DigitalOceanApiLib\Models\AuthPlugin;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Role;

$user = UserBuilder::init(
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
    ->build();
```



