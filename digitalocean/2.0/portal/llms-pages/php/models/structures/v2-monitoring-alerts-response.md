# V2 Monitoring Alerts Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2MonitoringAlertsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `policies` | [`Policy[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/policy.md) | Required | - | getPolicies(): array | setPolicies(array policies): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2MonitoringAlertsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\PolicyBuilder;
use DigitalOceanApiLib\Models\Builders\AlertsBuilder;
use DigitalOceanApiLib\Models\Builders\SlackBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Compare;
use DigitalOceanApiLib\Models\Type17;
use DigitalOceanApiLib\Models\Window1;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2MonitoringAlertsResponse = V2MonitoringAlertsResponseBuilder::init(
    [
        PolicyBuilder::init(
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
            '78b3da62-27e5-49ba-ac70-5db0b5935c64',
            80,
            Window1::ENUM_5M
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    MetaBuilder::init(
        1
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('last6')
                    ->next('next2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



