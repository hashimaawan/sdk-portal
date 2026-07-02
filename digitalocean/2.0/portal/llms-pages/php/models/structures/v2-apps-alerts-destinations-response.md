# V2 Apps Alerts Destinations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsAlertsDestinationsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `alert` | [`?Alert1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/alert-1.md) | Optional | - | getAlert(): ?Alert1 | setAlert(?Alert1 alert): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsAlertsDestinationsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\Alert1Builder;
use DigitalOceanApiLib\Models\Phase1;
use DigitalOceanApiLib\Models\Builders\Progress2Builder;
use DigitalOceanApiLib\Models\Builders\StepsOfAnAlertSProgressBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\ReasonBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status2;

$v2AppsAlertsDestinationsResponse = V2AppsAlertsDestinationsResponseBuilder::init()
    ->alert(
        Alert1Builder::init()
            ->componentName('component_name2')
            ->emails(
                [
                    'emails9'
                ]
            )
            ->id('id0')
            ->phase(Phase1::CONFIGURING)
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
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



