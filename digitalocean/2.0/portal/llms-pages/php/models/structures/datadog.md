# Datadog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGFkb2c

DataDog configuration.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Datadog`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `apiKey` | `string` | Required | Datadog API key. | getApiKey(): string | setApiKey(string apiKey): void |
| `endpoint` | `?string` | Optional | Datadog HTTP log intake endpoint. | getEndpoint(): ?string | setEndpoint(?string endpoint): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\DatadogBuilder;
use DigitalOceanApiLib\ApiHelper;

$datadog = DatadogBuilder::init(
    'abcdefghijklmnopqrstuvwxyz0123456789'
)
    ->endpoint('https://mydatadogendpoint.com')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



