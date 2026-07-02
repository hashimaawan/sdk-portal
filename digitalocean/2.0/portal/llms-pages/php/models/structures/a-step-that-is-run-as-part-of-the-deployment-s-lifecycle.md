# A Step that Is Run as Part of the Deployment S Lifecycle

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkElMjUyMHN0ZXAlMjUyMHRoYXQlMjUyMGlzJTI1MjBydW4lMjUyMGFzJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhlJTI1MjBkZXBsb3ltZW50JTI1MjdzJTI1MjBsaWZlY3ljbGU

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`AStepThatIsRunAsPartOfTheDeploymentSLifecycle`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `componentName` | `?string` | Optional | - | getComponentName(): ?string | setComponentName(?string componentName): void |
| `endedAt` | `?DateTime` | Optional | - | getEndedAt(): ?\DateTime | setEndedAt(?\DateTime endedAt): void |
| `messageBase` | `?string` | Optional | The base of a human-readable description of the step intended to be combined with the component name for presentation. For example:<br><br>`message_base` = "Building service"<br>`component_name` = "api" | getMessageBase(): ?string | setMessageBase(?string messageBase): void |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `reason` | [`?Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/reason.md) | Optional | - | getReason(): ?Reason | setReason(?Reason reason): void |
| `startedAt` | `?DateTime` | Optional | - | getStartedAt(): ?\DateTime | setStartedAt(?\DateTime startedAt): void |
| `status` | [`?string(Status2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-2.md) | Optional | **Default**: `Status2::UNKNOWN` | getStatus(): ?string | setStatus(?string status): void |
| `steps` | [`?(array[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | getSteps(): ?array | setSteps(?array steps): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\AStepThatIsRunAsPartOfTheDeploymentSLifecycleBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\ReasonBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status2;

$aStepThatIsRunAsPartOfTheDeploymentSLifecycle = AStepThatIsRunAsPartOfTheDeploymentSLifecycleBuilder::init()
    ->componentName('component')
    ->endedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-19T20:27:18Z'))
    ->messageBase('Building service')
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



