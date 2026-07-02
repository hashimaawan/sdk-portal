# V2 Uptime Checks Alerts Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2UptimeChecksAlertsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `comparison` | [`?string(Comparison)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/comparison.md) | Optional | The comparison operator used against the alert's threshold. | getComparison(): ?string | setComparison(?string comparison): void |
| `name` | `?string` | Optional | A human-friendly display name. | getName(): ?string | setName(?string name): void |
| `notifications` | [`?Notifications`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/notifications.md) | Optional | The notification settings for a trigger alert. | getNotifications(): ?Notifications | setNotifications(?Notifications notifications): void |
| `period` | [`?string(Period)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/period.md) | Optional | Period of time the threshold must be exceeded to trigger the alert. | getPeriod(): ?string | setPeriod(?string period): void |
| `threshold` | `?int` | Optional | The threshold at which the alert will enter a trigger state. The specific threshold is dependent on the alert type. | getThreshold(): ?int | setThreshold(?int threshold): void |
| `type` | [`?string(Type20)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-20.md) | Optional | The type of alert. | getType(): ?string | setType(?string type): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2UptimeChecksAlertsRequestBuilder;
use DigitalOceanApiLib\Models\Comparison;
use DigitalOceanApiLib\Models\Builders\NotificationsBuilder;
use DigitalOceanApiLib\Models\Builders\SlackBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Period;
use DigitalOceanApiLib\Models\Type20;

$v2UptimeChecksAlertsRequest = V2UptimeChecksAlertsRequestBuilder::init()
    ->comparison(Comparison::GREATER_THAN)
    ->name('Landing page degraded performance')
    ->notifications(
        NotificationsBuilder::init(
            [
                'email4',
                'email3'
            ],
            [
                SlackBuilder::init(
                    'channel6',
                    'url2'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                SlackBuilder::init(
                    'channel6',
                    'url2'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                SlackBuilder::init(
                    'channel6',
                    'url2'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->period(Period::ENUM_2M)
    ->threshold(300)
    ->type(Type20::LATENCY)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



