# Diagnostic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRpYWdub3N0aWM

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Diagnostic`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkName` | `?string` | Optional | The clusterlint check that resulted in the diagnostic. | getCheckName(): ?string | setCheckName(?string checkName): void |
| `message` | `?string` | Optional | Feedback about the object for users to fix. | getMessage(): ?string | setMessage(?string message): void |
| `object` | [`?Object`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | Metadata about the Kubernetes API object the diagnostic is reported on. | getObject(): ?Object | setObject(?Object object): void |
| `severity` | `?string` | Optional | Can be one of error, warning or suggestion. | getSeverity(): ?string | setSeverity(?string severity): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\DiagnosticBuilder;
use DigitalOceanApiLib\Models\Builders\ObjectBuilder;
use DigitalOceanApiLib\ApiHelper;

$diagnostic = DiagnosticBuilder::init()
    ->checkName('unused-config-map')
    ->message('Unused config map')
    ->object(
        ObjectBuilder::init()
            ->kind('kind0')
            ->name('name2')
            ->namespace('namespace0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->severity('warning')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



