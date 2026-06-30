# Section

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlNlY3Rpb24

*This model accepts additional fields of type array.*


# Class Name

`Section`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?string` | Optional | - | getId(): ?string | setId(?string id): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\SectionBuilder;
use M1PasswordConnectLib\ApiHelper;

$section = SectionBuilder::init()
    ->id('id6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



