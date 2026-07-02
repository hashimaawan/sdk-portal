# V2 Uptime Checks Alerts Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2UptimeChecksAlertsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `alert` | [`?Alerts1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/alerts-1.md) | Optional | - | getAlert(): ?Alerts1 | setAlert(?Alerts1 alert): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2UptimeChecksAlertsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\Alerts1Builder;
use DigitalOceanApiLib\Models\Comparison;
use DigitalOceanApiLib\Models\Builders\NotificationsBuilder;
use DigitalOceanApiLib\Models\Builders\SlackBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Period;

$v2UptimeChecksAlertsResponse1 = V2UptimeChecksAlertsResponse1Builder::init()
    ->alert(
        Alerts1Builder::init()
            ->id('00002454-0000-0000-0000-000000000000')
            ->comparison(Comparison::GREATER_THAN)
            ->name('name0')
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
            ->period(Period::ENUM_30M)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



