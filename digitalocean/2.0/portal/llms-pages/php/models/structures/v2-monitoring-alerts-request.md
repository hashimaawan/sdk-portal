# V2 Monitoring Alerts Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2MonitoringAlertsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `alerts` | [`Alerts`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/alerts.md) | Required | - | getAlerts(): Alerts | setAlerts(Alerts alerts): void |
| `compare` | [`string(Compare)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/compare.md) | Required | - | getCompare(): string | setCompare(string compare): void |
| `description` | `string` | Required | - | getDescription(): string | setDescription(string description): void |
| `enabled` | `bool` | Required | - | getEnabled(): bool | setEnabled(bool enabled): void |
| `entities` | `string[]` | Required | - | getEntities(): array | setEntities(array entities): void |
| `tags` | `string[]` | Required | - | getTags(): array | setTags(array tags): void |
| `type` | [`string(Type17)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-17.md) | Required | - | getType(): string | setType(string type): void |
| `value` | `float` | Required | - | getValue(): float | setValue(float value): void |
| `window` | [`string(Window1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/window-1.md) | Required | - | getWindow(): string | setWindow(string window): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2MonitoringAlertsRequestBuilder;
use DigitalOceanApiLib\Models\Builders\AlertsBuilder;
use DigitalOceanApiLib\Models\Builders\SlackBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Compare;
use DigitalOceanApiLib\Models\Type17;
use DigitalOceanApiLib\Models\Window1;

$v2MonitoringAlertsRequest = V2MonitoringAlertsRequestBuilder::init(
    AlertsBuilder::init(
        [
            'bob@exmaple.com'
        ],
        [
            SlackBuilder::init(
                'Production Alerts',
                'https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    Compare::GREATERTHAN,
    'CPU Alert',
    true,
    [
        '192018292'
    ],
    [
        'droplet_tag'
    ],
    Type17::ENUM_V1INSIGHTSDROPLETCPU,
    80,
    Window1::ENUM_5M
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



