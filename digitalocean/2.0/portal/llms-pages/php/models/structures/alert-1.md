# Alert 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFsZXJ0MQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Alert1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `componentName` | `?string` | Optional | - | getComponentName(): ?string | setComponentName(?string componentName): void |
| `emails` | `?(string[])` | Optional | - | getEmails(): ?array | setEmails(?array emails): void |
| `id` | `?string` | Optional, Read-only | - | getId(): ?string | setId(?string id): void |
| `phase` | [`?string(Phase1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/phase-1.md) | Optional | **Default**: `Phase1::UNKNOWN` | getPhase(): ?string | setPhase(?string phase): void |
| `progress` | [`?Progress2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/progress-2.md) | Optional | - | getProgress(): ?Progress2 | setProgress(?Progress2 progress): void |
| `slackWebhooks` | [`?(SlackWebhooksToSendAlertsTo[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - | getSlackWebhooks(): ?array | setSlackWebhooks(?array slackWebhooks): void |
| `spec` | [`?Alert`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/alert.md) | Optional | - | getSpec(): ?Alert | setSpec(?Alert spec): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Alert1Builder;
use DigitalOceanApiLib\Models\Phase1;
use DigitalOceanApiLib\Models\Builders\Progress2Builder;
use DigitalOceanApiLib\Models\Builders\StepsOfAnAlertSProgressBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\ReasonBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status2;

$alert1 = Alert1Builder::init()
    ->componentName('backend')
    ->emails(
        [
            'sammy@digitalocean.com'
        ]
    )
    ->id('4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf')
    ->phase(Phase1::ACTIVE)
    ->progress(
        Progress2Builder::init()
            ->steps(
                [
                    StepsOfAnAlertSProgressBuilder::init()
                        ->endedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->name('name2')
                        ->reason(
                            ReasonBuilder::init()
                                ->code('code2')
                                ->message('message4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->startedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->status(Status2::SUCCESS)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    StepsOfAnAlertSProgressBuilder::init()
                        ->endedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->name('name2')
                        ->reason(
                            ReasonBuilder::init()
                                ->code('code2')
                                ->message('message4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->startedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->status(Status2::SUCCESS)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    StepsOfAnAlertSProgressBuilder::init()
                        ->endedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->name('name2')
                        ->reason(
                            ReasonBuilder::init()
                                ->code('code2')
                                ->message('message4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->startedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->status(Status2::SUCCESS)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



