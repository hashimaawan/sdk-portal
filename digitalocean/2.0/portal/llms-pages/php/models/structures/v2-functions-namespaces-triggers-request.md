# V2 Functions Namespaces Triggers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `function` | `string` | Required | Name of function(action) that exists in the given namespace. | getFunction(): string | setFunction(string function): void |
| `isEnabled` | `bool` | Required | Indicates weather the trigger is paused or unpaused. | getIsEnabled(): bool | setIsEnabled(bool isEnabled): void |
| `name` | `string` | Required | The trigger's unique name within the namespace. | getName(): string | setName(string name): void |
| `scheduledDetails` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/scheduled-details.md) | Required | Trigger details for SCHEDULED type, where body is optional. | getScheduledDetails(): ScheduledDetails | setScheduledDetails(ScheduledDetails scheduledDetails): void |
| `type` | `string` | Required | One of different type of triggers. Currently only SCHEDULED is supported. | getType(): string | setType(string type): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2FunctionsNamespacesTriggersRequestBuilder;
use DigitalOceanApiLib\Models\Builders\ScheduledDetailsBuilder;
use DigitalOceanApiLib\Models\Builders\BodyBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2FunctionsNamespacesTriggersRequest = V2FunctionsNamespacesTriggersRequestBuilder::init(
    'hello',
    true,
    'my trigger',
    ScheduledDetailsBuilder::init(
        '* * * * *'
    )
        ->body(
            BodyBuilder::init()
                ->name('name6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    'SCHEDULED'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



