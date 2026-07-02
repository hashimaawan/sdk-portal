# Pgbouncer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlBnYm91bmNlcg

PGBouncer connection pooling settings

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Pgbouncer`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `autodbIdleTimeout` | `?int` | Optional | If the automatically-created database pools have been unused this many seconds, they are freed. If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` | getAutodbIdleTimeout(): ?int | setAutodbIdleTimeout(?int autodbIdleTimeout): void |
| `autodbMaxDbConnections` | `?int` | Optional | Only allows a maximum this many server connections per database (regardless of user). If 0, allows unlimited connections.<br><br>**Constraints**: `>= 0`, `<= 2147483647` | getAutodbMaxDbConnections(): ?int | setAutodbMaxDbConnections(?int autodbMaxDbConnections): void |
| `autodbPoolMode` | [`?string(AutodbPoolMode)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/autodb-pool-mode.md) | Optional | PGBouncer pool mode | getAutodbPoolMode(): ?string | setAutodbPoolMode(?string autodbPoolMode): void |
| `autodbPoolSize` | `?int` | Optional | If non-zero, automatically creates a pool of that size per user when a pool doesn't exist.<br><br>**Constraints**: `>= 0`, `<= 10000` | getAutodbPoolSize(): ?int | setAutodbPoolSize(?int autodbPoolSize): void |
| `ignoreStartupParameters` | [`?(string(IgnoreStartupParameter)[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/ignore-startup-parameter.md) | Optional | List of parameters to ignore when given in startup packet.<br><br>**Constraints**: *Maximum Items*: `32` | getIgnoreStartupParameters(): ?array | setIgnoreStartupParameters(?array ignoreStartupParameters): void |
| `minPoolSize` | `?int` | Optional | If current server connections are below this number, adds more. Improves behavior when usual load comes suddenly back after period of total inactivity. The value is effectively capped at the pool size.<br><br>**Constraints**: `>= 0`, `<= 10000` | getMinPoolSize(): ?int | setMinPoolSize(?int minPoolSize): void |
| `serverIdleTimeout` | `?int` | Optional | Drops server connections if they have been idle more than this many seconds.  If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` | getServerIdleTimeout(): ?int | setServerIdleTimeout(?int serverIdleTimeout): void |
| `serverLifetime` | `?int` | Optional | The pooler closes any unused server connection that has been connected longer than this amount of seconds.<br><br>**Constraints**: `>= 60`, `<= 86400` | getServerLifetime(): ?int | setServerLifetime(?int serverLifetime): void |
| `serverResetQueryAlways` | `?bool` | Optional | Run server_reset_query (DISCARD ALL) in all pooling modes. | getServerResetQueryAlways(): ?bool | setServerResetQueryAlways(?bool serverResetQueryAlways): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\PgbouncerBuilder;
use DigitalOceanApiLib\Models\AutodbPoolMode;
use DigitalOceanApiLib\Models\IgnoreStartupParameter;
use DigitalOceanApiLib\ApiHelper;

$pgbouncer = PgbouncerBuilder::init()
    ->autodbIdleTimeout(3600)
    ->autodbMaxDbConnections(1)
    ->autodbPoolMode(AutodbPoolMode::SESSION)
    ->autodbPoolSize(1)
    ->ignoreStartupParameters(
        [
            IgnoreStartupParameter::EXTRA_FLOAT_DIGITS,
            IgnoreStartupParameter::SEARCH_PATH
        ]
    )
    ->minPoolSize(1)
    ->serverIdleTimeout(600)
    ->serverLifetime(3600)
    ->serverResetQueryAlways(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



