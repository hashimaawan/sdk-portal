# V2 Functions Namespaces Triggers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `trigger` | [`?Trigger`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/trigger.md) | Optional | - | getTrigger(): ?Trigger | setTrigger(?Trigger trigger): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2FunctionsNamespacesTriggersResponse1Builder;
use DigitalOceanApiLib\Models\Builders\TriggerBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2FunctionsNamespacesTriggersResponse1 = V2FunctionsNamespacesTriggersResponse1Builder::init()
    ->trigger(
        TriggerBuilder::init()
            ->createdAt('created_at6')
            ->function('function6')
            ->isEnabled(false)
            ->name('name8')
            ->namespace('namespace4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



