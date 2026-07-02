# Configurations for External Logging

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb25zJTI1MjBmb3IlMjUyMGV4dGVybmFsJTI1MjBsb2dnaW5nLg

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`ConfigurationsForExternalLogging`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `datadog` | [`?Datadog`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/datadog.md) | Optional | DataDog configuration. | getDatadog(): ?Datadog | setDatadog(?Datadog datadog): void |
| `logtail` | [`?Logtail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/logtail.md) | Optional | Logtail configuration. | getLogtail(): ?Logtail | setLogtail(?Logtail logtail): void |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `2`, *Maximum Length*: `42`, *Pattern*: `^[A-Za-z0-9()\[\]'"][-A-Za-z0-9_. \/()\[\]]{0,40}[A-Za-z0-9()\[\]'"]$` | getName(): string | setName(string name): void |
| `papertrail` | [`?Papertrail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/papertrail.md) | Optional | Papertrail configuration. | getPapertrail(): ?Papertrail | setPapertrail(?Papertrail papertrail): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ConfigurationsForExternalLoggingBuilder;
use DigitalOceanApiLib\Models\Builders\DatadogBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\LogtailBuilder;
use DigitalOceanApiLib\Models\Builders\PapertrailBuilder;

$configurationsForExternalLogging = ConfigurationsForExternalLoggingBuilder::init(
    'my_log_destination'
)
    ->datadog(
        DatadogBuilder::init(
            'api_key2'
        )
            ->endpoint('endpoint8')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->logtail(
        LogtailBuilder::init()
            ->token('token4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->papertrail(
        PapertrailBuilder::init(
            'endpoint4'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



