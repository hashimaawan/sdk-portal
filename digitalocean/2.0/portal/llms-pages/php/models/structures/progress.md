# Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlByb2dyZXNz

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Progress`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `errorSteps` | `?int` | Optional | - | getErrorSteps(): ?int | setErrorSteps(?int errorSteps): void |
| `pendingSteps` | `?int` | Optional | - | getPendingSteps(): ?int | setPendingSteps(?int pendingSteps): void |
| `runningSteps` | `?int` | Optional | - | getRunningSteps(): ?int | setRunningSteps(?int runningSteps): void |
| `steps` | [`?(AStepThatIsRunAsPartOfTheDeploymentSLifecycle[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - | getSteps(): ?array | setSteps(?array steps): void |
| `successSteps` | `?int` | Optional | - | getSuccessSteps(): ?int | setSuccessSteps(?int successSteps): void |
| `summarySteps` | [`?(AStepThatIsRunAsPartOfTheDeploymentSLifecycle[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - | getSummarySteps(): ?array | setSummarySteps(?array summarySteps): void |
| `totalSteps` | `?int` | Optional | - | getTotalSteps(): ?int | setTotalSteps(?int totalSteps): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ProgressBuilder;
use DigitalOceanApiLib\Models\Builders\AStepThatIsRunAsPartOfTheDeploymentSLifecycleBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\ReasonBuilder;
use DigitalOceanApiLib\ApiHelper;

$progress = ProgressBuilder::init()
    ->errorSteps(3)
    ->pendingSteps(2)
    ->runningSteps(2)
    ->steps(
        [
            AStepThatIsRunAsPartOfTheDeploymentSLifecycleBuilder::init()
                ->componentName('component_name0')
                ->endedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->messageBase('message_base4')
                ->name('name2')
                ->reason(
                    ReasonBuilder::init()
                        ->code('code2')
                        ->message('message4')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            AStepThatIsRunAsPartOfTheDeploymentSLifecycleBuilder::init()
                ->componentName('component_name0')
                ->endedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->messageBase('message_base4')
                ->name('name2')
                ->reason(
                    ReasonBuilder::init()
                        ->code('code2')
                        ->message('message4')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            AStepThatIsRunAsPartOfTheDeploymentSLifecycleBuilder::init()
                ->componentName('component_name0')
                ->endedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->messageBase('message_base4')
                ->name('name2')
                ->reason(
                    ReasonBuilder::init()
                        ->code('code2')
                        ->message('message4')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->successSteps(4)
    ->totalSteps(5)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



