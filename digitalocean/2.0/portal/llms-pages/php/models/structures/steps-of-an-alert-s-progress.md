# Steps of an Alert S Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN0ZXBzJTI1MjBvZiUyNTIwYW4lMjUyMGFsZXJ0JTI1MjdzJTI1MjBwcm9ncmVzcy4

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`StepsOfAnAlertSProgress`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `endedAt` | `?DateTime` | Optional | - | getEndedAt(): ?\DateTime | setEndedAt(?\DateTime endedAt): void |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `reason` | [`?Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/reason.md) | Optional | - | getReason(): ?Reason | setReason(?Reason reason): void |
| `startedAt` | `?DateTime` | Optional | - | getStartedAt(): ?\DateTime | setStartedAt(?\DateTime startedAt): void |
| `status` | [`?string(Status2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-2.md) | Optional | **Default**: `Status2::UNKNOWN` | getStatus(): ?string | setStatus(?string status): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\StepsOfAnAlertSProgressBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\ReasonBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status2;

$stepsOfAnAlertSProgress = StepsOfAnAlertSProgressBuilder::init()
    ->endedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-19T20:27:18Z'))
    ->name('example_step')
    ->reason(
        ReasonBuilder::init()
            ->code('code2')
            ->message('message4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->startedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-19T20:27:18Z'))
    ->status(Status2::SUCCESS)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



