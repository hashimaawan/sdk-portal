# V2 Monitoring Alerts Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2MonitoringAlertsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `policy` | [`?Policy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/policy.md) | Optional | - | getPolicy(): ?Policy | setPolicy(?Policy policy): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2MonitoringAlertsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\PolicyBuilder;
use DigitalOceanApiLib\Models\Builders\AlertsBuilder;
use DigitalOceanApiLib\Models\Builders\SlackBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Compare;
use DigitalOceanApiLib\Models\Type17;
use DigitalOceanApiLib\Models\Window1;

$v2MonitoringAlertsResponse1 = V2MonitoringAlertsResponse1Builder::init()
    ->policy(
        PolicyBuilder::init(
            AlertsBuilder::init(
                [
                    'email2',
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
                ->build(),
            Compare::GREATERTHAN,
            'description4',
            false,
            [
                'entities9'
            ],
            [
                'tags9',
                'tags0',
                'tags1'
            ],
            Type17::ENUM_V1INSIGHTSDROPLETDISK_READ,
            'uuid0',
            149.36,
            Window1::ENUM_30M
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



