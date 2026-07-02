# V2 Databases Online Migration Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesOnlineMigrationRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `disableSsl` | `?bool` | Optional | Enables SSL encryption when connecting to the source database. | getDisableSsl(): ?bool | setDisableSsl(?bool disableSsl): void |
| `source` | [`?Source`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/source.md) | Optional | - | getSource(): ?Source | setSource(?Source source): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesOnlineMigrationRequestBuilder;
use DigitalOceanApiLib\Models\Builders\SourceBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2DatabasesOnlineMigrationRequest = V2DatabasesOnlineMigrationRequestBuilder::init()
    ->disableSsl(false)
    ->source(
        SourceBuilder::init()
            ->database('database4')
            ->host('host4')
            ->password('password8')
            ->port(180)
            ->ssl(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



