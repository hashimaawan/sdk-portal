# Trigger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlRyaWdnZXI

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Trigger`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?string` | Optional | UTC time string. | getCreatedAt(): ?string | setCreatedAt(?string createdAt): void |
| `function` | `?string` | Optional | Name of function(action) that exists in the given namespace. | getFunction(): ?string | setFunction(?string function): void |
| `isEnabled` | `?bool` | Optional | Indicates weather the trigger is paused or unpaused. | getIsEnabled(): ?bool | setIsEnabled(?bool isEnabled): void |
| `name` | `?string` | Optional | The trigger's unique name within the namespace. | getName(): ?string | setName(?string name): void |
| `namespace` | `?string` | Optional | A unique string format of UUID with a prefix fn-. | getNamespace(): ?string | setNamespace(?string namespace): void |
| `scheduledDetails` | [`?ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. | getScheduledDetails(): ?ScheduledDetails | setScheduledDetails(?ScheduledDetails scheduledDetails): void |
| `scheduledRuns` | [`?ScheduledRuns`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/scheduled-runs.md) | Optional | - | getScheduledRuns(): ?ScheduledRuns | setScheduledRuns(?ScheduledRuns scheduledRuns): void |
| `type` | `?string` | Optional | String which indicates the type of trigger source like SCHEDULED. | getType(): ?string | setType(?string type): void |
| `updatedAt` | `?string` | Optional | UTC time string. | getUpdatedAt(): ?string | setUpdatedAt(?string updatedAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\TriggerBuilder;
use DigitalOceanApiLib\ApiHelper;

$trigger = TriggerBuilder::init()
    ->createdAt('2022-11-11T04:16:45Z')
    ->function('hello')
    ->isEnabled(true)
    ->name('my trigger')
    ->namespace('fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx')
    ->type('SCHEDULED')
    ->updatedAt('2022-11-11T04:16:45Z')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



