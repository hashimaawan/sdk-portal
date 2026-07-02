# Scheduled Details

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlNjaGVkdWxlZERldGFpbHM

Trigger details for SCHEDULED type, where body is optional.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`ScheduledDetails`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `body` | [`?Body`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/body.md) | Optional | Optional data to be sent to function while triggering the function. | getBody(): ?Body | setBody(?Body body): void |
| `cron` | `string` | Required | valid cron expression string which is required for SCHEDULED type triggers. | getCron(): string | setCron(string cron): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ScheduledDetailsBuilder;
use DigitalOceanApiLib\Models\Builders\BodyBuilder;
use DigitalOceanApiLib\ApiHelper;

$scheduledDetails = ScheduledDetailsBuilder::init(
    '* * * * *'
)
    ->body(
        BodyBuilder::init()
            ->name('name6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



