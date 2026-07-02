# V2 Functions Namespaces Triggers Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `isEnabled` | `?bool` | Optional | Indicates weather the trigger is paused or unpaused. | getIsEnabled(): ?bool | setIsEnabled(?bool isEnabled): void |
| `scheduledDetails` | [`?ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. | getScheduledDetails(): ?ScheduledDetails | setScheduledDetails(?ScheduledDetails scheduledDetails): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2FunctionsNamespacesTriggersRequest1Builder;
use DigitalOceanApiLib\Models\Builders\ScheduledDetailsBuilder;
use DigitalOceanApiLib\Models\Builders\BodyBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2FunctionsNamespacesTriggersRequest1 = V2FunctionsNamespacesTriggersRequest1Builder::init()
    ->isEnabled(true)
    ->scheduledDetails(
        ScheduledDetailsBuilder::init(
            'cron2'
        )
            ->body(
                BodyBuilder::init()
                    ->name('name6')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



